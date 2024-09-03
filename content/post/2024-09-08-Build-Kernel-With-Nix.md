+++
author = "Vunny Sodhi"
title = "Build custom kernel with Nix"
date = "2024-09-08"
description = "Build kernel with Nix"
tags = [
    "nix",
    "kernel",
]
+++

This guide of building drm-tip kernel using Nix
<!--more-->
#### You can create derivation 
```
boot.kernelPackages =
    let
    linux_pkg =
        { fetchgit, buildLinux, ... }@args:

        buildLinux (
        args
        // rec {
            version = "6.11.0-rc6";

            src = fetchgit {
            url = "https://anongit.freedesktop.org/git/drm-tip.git/";
            rev = "f9638b76f51e30fcb4ef993f484212f2d338488b";
            sha256 = "sha256-tzPt1zax7e1SV7y6zRJNiAF7eNvOx0yv4Papkegx7L8=";
            };
        }
        // (args.argsOverride or { })

        );
    linux_6-11-0 = pkgs.callPackage linux_pkg { };
    in
    pkgs.recurseIntoAttrs (pkgs.linuxPackagesFor linux_6-11-0);
```

#### References:
Tarball Download link: https://mirrors.edge.kernel.org/pub/linux/kernel/v6.x/
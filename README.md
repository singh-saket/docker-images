# Troubleshoot Docker & Sitecore Images

## Overview

Welcome to the repository for Troubleshoot Docker & Sitecore Images. This repository contains the output of the various sitecore images after executing the troubleshooting commands.

### 1] sitecore-xp0-cm.json

I was facing an issue with the "sitecore-xp0-cm" sitecore image after taking the latest image pull, and for this reason, I executed the following PowerShell command:

<pre>
  docker image inspect --format '{{json .}}' "Add your image id here" '. | {Id: .Id, Digest: .Digest, RepoDigests: .RepoDigests, Labels: .Config.Labels}'
</pre>

**Note:** We have to provide the specific image "ID" in the command.

The above command produces the output in "Json" format, as shown in the "sitecore-xp0-cm.json" file. In this way, it becaumes easy to check and debug the image and its implementation with details is explained in the following blogpost.

**Blog Title :** Troubleshooting Sitecore Image Update Issue

**Blog Url :** https://blogs.perficient.com/2023/11/15/troubleshooting-sitecore-image-update-issue/

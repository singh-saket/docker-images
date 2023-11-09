# Troubleshoot-Sitecore-Images

This repository contains the output of the various sitecore images after executing the troubleshooting commands.

1] sitecore-xp0-cm.json

I was facing an issue with the "sitecore-xp0-cm" sitecore image after taking the latest image pull, and for this reason, I executed the following PowerShell command:

<pre>
  docker image inspect --format '{{json .}}' "Add your image id here" '. | {Id: .Id, Digest: .Digest, RepoDigests: .RepoDigests, Labels: .Config.Labels}'
</pre>

Note: We have to provide the specific image "ID" in the command.

The above command produces the output in "Json" format, as shown in the "sitecore-xp0-cm.json" file. In this way, it becaumes easy to check and debug the image.

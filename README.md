<html><!--head>
 <style>
 .alignnone {
  max-width: 100%;
  height: auto;
  display: block; /* To prevent inline default space below images */
}
</style>
</head-->
<h2 dir="auto" tabindex="-1">Environments and Technologies Used</h2>
<ul>
 	<li>Microsoft Azure (Virtual Machines/Domain Controller/Client Machine)</li>
 	<li>Remote Desktop</li>
 	<li>Shared Network Files</li>
</ul>
&nbsp;
<h3 dir="auto" tabindex="-1" align="center">Setup Resources in Azure</h3>
<ul>
 	<li dir="auto" tabindex="-1">We will be setting up shared network files and permissions in this lab. We need to create four folders on the DC-1 VM - "read-access", "read/write-access", "no-access", and "LABACCESS". Certain files will have specific permissions, and only designated people will be able to access them. Let's begin by navigating to the C:/ drive on the DC-1 machine and creating these four folders.</li>
</ul>
<a href="https://vikaspatel.tech/wp-content/uploads/2023/04/6-1.png">
  <img class="alignnone size-full wp-image-180" src="https://vikaspatel.tech/wp-content/uploads/2023/04/6-1.png" alt="" />
</a>
<ul>
 	<li>Once the folders have been created, the next step is to share them on the network so that client-1 machine can access them. We also need to set the appropriate permissions for each folder in DC-1. For instance, "read-access" folder should have read-only permissions for domain users, "read/write access" folder should have read/write permissions for domain users, and "no-access" folder should have read/write permissions for domain admins only.</li>
</ul>

<a href="https://vikaspatel.tech/wp-content/uploads/2023/04/6-1.png">
  <img class="alignnone size-full wp-image-180" src="https://vikaspatel.tech/wp-content/uploads/2023/04/1-2.png" alt="" />
</a><div class="group w-full text-gray-800 dark:text-gray-100 border-b border-black/10 dark:border-gray-900/50 bg-gray-50 dark:bg-[#444654]">
<div class="text-base gap-4 md:gap-6 md:max-w-2xl lg:max-w-xl xl:max-w-3xl p-4 md:py-6 flex lg:px-0 m-auto">
<div class="relative flex w-[calc(100%-50px)] flex-col gap-1 md:gap-3 lg:w-[calc(100%-115px)]">
<div class="flex flex-grow flex-col gap-3">
<div class="min-h-[20px] flex flex-col items-start gap-4 whitespace-pre-wrap">
<div class="markdown prose w-full break-words dark:prose-invert light">
<ul>
 	<li>We can confirm that the permissions we set are working correctly by testing the shared files on the client machine using a regular user account.</li>
</ul>
</div>
</div>
</div>
<div class="flex justify-between lg:block">
<div class="text-gray-400 flex self-end lg:self-center justify-center mt-2 gap-2 md:gap-3 lg:gap-1 lg:absolute lg:top-0 lg:translate-x-full lg:right-0 lg:mt-0 lg:pl-2 visible"><a href="https://vikaspatel.tech/wp-content/uploads/2023/04/7-1.png">
  <img class="alignnone size-full wp-image-180" src="https://vikaspatel.tech/wp-content/uploads/2023/04/7-1.png" alt="" />
</a></div>
<div></div>
</div>
<div class="group w-full text-gray-800 dark:text-gray-100 border-b border-black/10 dark:border-gray-900/50 bg-gray-50 dark:bg-[#444654]">
<div class="text-base gap-4 md:gap-6 md:max-w-2xl lg:max-w-xl xl:max-w-3xl p-4 md:py-6 flex lg:px-0 m-auto">
<div class="relative flex w-[calc(100%-50px)] flex-col gap-1 md:gap-3 lg:w-[calc(100%-115px)]">
<div class="flex flex-grow flex-col gap-3">
<div class="min-h-[20px] flex flex-col items-start gap-4 whitespace-pre-wrap">
<div class="markdown prose w-full break-words dark:prose-invert light">
<ul>
 	<li>Let's go back to the DC-1 VM and create a security group called "LABACCESS" in Active Directory. Only users assigned to this security group will be permitted to access the "LABACCESS" folder. We will need to share the "LABACCESS" folder, similar to the previous section, but this time we will only share it with the "LABACCESS" group. Regular users will not have access to this folder. If we want to give a regular user access to the accounting folder, they must first be added to the "LABACCESS" security group.</li>
</ul>
</div>
</div>
<div class="min-h-[20px] flex flex-col items-start gap-4 whitespace-pre-wrap">
<div class="markdown prose w-full break-words dark:prose-invert light">

<a href="https://vikaspatel.tech/wp-content/uploads/2023/04/3-1.png">
  <img class="alignnone size-full wp-image-180" src="https://vikaspatel.tech/wp-content/uploads/2023/04/3-1.png" alt="" />
</a>
<a href="https://vikaspatel.tech/wp-content/uploads/2023/04/4-1.png">
  <img class="alignnone size-full wp-image-180" src="https://vikaspatel.tech/wp-content/uploads/2023/04/4-1.png" alt="" />
</a>
<a href="https://vikaspatel.tech/wp-content/uploads/2023/04/5-2.png">
  <img class="alignnone size-full wp-image-180" src="https://vikaspatel.tech/wp-content/uploads/2023/04/5-2.png" alt="" />
</a>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</html>

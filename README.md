# What is Parasite?
Parasite is a powerful code insertion platform for OS X. It enables developers to easily create extensions which change the original behavior of functions. For users Parasite provides an easy way to install these extensions and tweak their OS.

# How does Parasite work?
Parasite consists of various components which altogether provide a safe and smooth experience. Here’s a short overview:

## Parasite.kext
This is the core component of Parasite, a kernel extension. It injects ParasiteLoader.dylib into every process that is executed after the kext is loaded.

## ParasiteLoader.dylib
This is the trampoline that gets injected by the kext. It handles extensions loading and excludes blacklisted processes and root processes.

## ParasiteRuntime.framework
This is a framework that makes developing extensions easy. It includes some nice macros, ZKSwizzle for hooking Obj-C functions and substitute by comex for hooking C functions.

# How do I install Parasite?
That’s pretty easy actually. Just disable kext validation via csrutil and paste ```curl -fsSL https://github.com/ParasiteTeam/installer/raw/master/install.sh | sudo bash``` into your terminal prompt.

# How do I install Extensions?
Extensions can be .bundle files or just a .plist. Installing them is mainly just putting them into their designated directory.

## I want to install an extension via bundle, bro?!
No problem, extensions are located at ```/Library/Parasite/Extensions```. Just put the .bundle file in there and it will be automatically loaded when the process it should inject into gets executed.

## I want to install a an extension via plist, bro?!
That’s cool. Runtime modification via a .plist is supported by Crucible. Crucible takes the information provided by the .plist and transforms them to code, so to say. The .plist files are located at ```/Library/Parasite/Crucible```.

# How do I create an extension?
You have two options to create extensions, which are the following:
## Bundle extension
TODO

## Crucible extension
TODO

# Something I didn’t think of
Soon, ayy.
---
title: Utilisation du Kit de développement Microsoft pour Java SDK
TOCTitle: Using the Microsoft SDK for Java
ms:assetid: 35a1adb2-06d6-ff45-f151-f1f60ff9bfe2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249116(v=office.15)
ms:contentKeyID: 48544152
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 03916c546d76fd9317729ea1a316d14cbabdbe3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588881"
---
# <a name="using-the-microsoft-sdk-for-java"></a>Utilisation du kit de développement logiciel Microsoft pour Java


**S’applique à** : Access 2013, Office 2013

Le Kit de développement Microsoft pour Java SDK est un kit conçu pour l'environnement Microsoft Internet Explorer. Des outils, des informations et des exemples sont fournis pour vous aider à développer des programmes et des applets Java basés sur JDK 1.1 et la machine virtuelle Microsoft Win32 (Microsoft VM). Le Kit de développement Microsoft pour Java SDK n'est pas lié à Microsoft Visual J++.

L'utilitaire Jactivex.exe génère les classes à partir d'une bibliothèque de types mais peut uniquement être appelé à partir d'une ligne de commande. Cette fonctionnalité n'est pas intégrée à l'environnement de développement Visual J++. Contrairement aux classes générées avec l'[Assistant Bibliothèque de types Java](using-the-java-type-library-wizard.md), vous pouvez intervenir sur les wrappers de classes créés par le Kit de développement. Ceci est utile lorsque vous déboguez votre code afin de déterminer comment il utilise les classes wrappers ADO.

Ce mécanisme lit la bibliothèque de types ADO et génère des classes que vous pouvez instancier au sein de votre application. Il génère ces classes à l’emplacement suivant \\ \<windows directory\> \\ : Java \\ trustlib \\ msado15.

La création d'une application ADO dans Java à l'aide du Kit de développement Microsoft pour Java SDK revient exactement, au niveau du code source, à utiliser l'Assistant Bibliothèque de types Java. Pour consulter un exemple de code, consultez [Wrappers de classe Java ADO](ado-java-class-wrappers.md). La seule différence est la façon dont vous générez les classes wrappers, comme l'illustrent les étapes suivantes.

**Pour créer un projet ADO avec le Kit de développement Microsoft pour Java SDK**

1.  Exécutez ce qui suit depuis une invite de commandes. Vous devez définir le chemin d'accès pour qu'il inclue le répertoire Bin du Kit de développement Microsoft pour Java SDK ou exécuter la commande depuis cet emplacement. En général, le Kit de développement Microsoft pour Java SDK est installé dans le même emplacement que Visual Studio. Il s'agit d'une instruction de commande unique.
    
    ```vb 
     
    \<path to DevStudio>\<path to Java SDK>\bin\JactiveX.exe /javatlb "C:\program files\common files\system\ado\msado15.dll" 
    ```

2.  Exécutez la commande suivante pour compiler les classes générées. Le commutateur /g:t active la génération des symboles de débogage pour que vous puissiez suivre les symboles .Java. Supprimez-le des versions release.
    
    ```vb 
     
    jvc /g:t c:\<windows>\Java\trustlib\msado15\*.Java 
    ```

3.  Pour utiliser ces fichiers, ouvrez votre projet dans Visual J++. Dans le menu **Projet**, choisissez **Ajouter au projet**. Sélectionnez **des** fichiers et ajoutez tous les fichiers. Fichiers JAVA générés dans le répertoire trustlib \\ msado15 de votre projet.


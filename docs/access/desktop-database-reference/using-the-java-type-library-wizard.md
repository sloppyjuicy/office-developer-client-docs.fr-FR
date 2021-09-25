---
title: Utilisation de l'Assistant Bibliothèque de types Java
TOCTitle: Using the Java Type Library Wizard
ms:assetid: 96af770c-c7c2-c905-3c3e-383a5b99cab2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249670(v=office.15)
ms:contentKeyID: 48546455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b47bc9254e441a7ccbba371aeea35c798f003402
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588888"
---
# <a name="using-the-java-type-library-wizard"></a>Utilisation de l’assistant de bibliothèque de type Java


**S’applique à** : Access 2013, Office 2013

L'Assistant Bibliothèque de types Java est une fonctionnalité de Visual J++ 1.x intégrée au menu **Outils** de l'environnement de développement. Il sert à effectuer des recherches dans une bibliothèque de types et à créer une interface Java qui permet d'accéder aux objets COM. Dans Visual J++ 6.0, l'Assistant Bibliothèque de types Java a été remplacé par [ADO pour Windows Foundation Classes](ado-wfc-programming.md).

L'Assistant Bibliothèque de types Java produit des résultats similaires aux outils de ligne de commande inclus avec le [Kit de développement Microsoft pour Java SDK](using-the-microsoft-sdk-for-java.md). Cependant, vous n'avez pas accès aux wrappers de classes que l'Assistant génère, contrairement aux wrappers de classe générés par le Kit de développement Microsoft pour Java SDK.

L Java De la bibliothèque de types génère les classes à l’emplacement \\ \<windows directory\> \\ suivant : Java \\ trustlib \\ msado15. Le fichier Summary.txt, situé dans le répertoire dans lequel les classes ont été générées, comporte les définitions de classes qu'il a générées.

L'Assistant Bibliothèque de types Java convertit les types énumérés, trouvés dans une bibliothèque de types donnée, en type INT (nombre entier). Il définit également une interface qui correspond à chaque type énuméré de la bibliothèque de types. Vous pouvez référencer les valeurs d'un type énuméré ADO au moyen de la syntaxe suivante :

```vb 
 
msado15.<Enum Name>.<constant Name> 
```

Un exemple de définition de la propriété **CommandType** d'un objet **Command** est illustré dans le fragment de code suivant :

```vb 
 
Cmd1.putCommandType( msado15.CommandTypeEnum.adCmdStoredProc ); 
```

Une autre solution consiste à hériter du wrapper de type énuméré généré par l'Assistant Bibliothèque de types Java. Dans ce cas, vous pouvez supprimer « msado15. » de la syntaxe. Cependant, votre classe doit hériter de chaque objet Java et interface de type énuméré qu'elle référence pour ne plus avoir à référencer msado15.\* devant tous les objets ADO et les valeurs énumérées.

Pour obtenir un exemple de code, consultez [Wrappers de classe Java ADO](ado-java-class-wrappers.md).

**Pour exécuter l’Java de bibliothèque de types à partir de Visual J++ version 1.*x***

1.  Depuis le menu **Outils**, sélectionnez **Assistant Bibliothèque de types Java**.

2.  Sélectionnez « Bibliothèque Microsoft ActiveX Data Objects », puis cliquez sur **OK**. This now (re)generates files in the \\ trustlib directory for ADO (by default at c: \\ winnt \\ java \\ trustlib \\ msado15). Si vous avez utilisé le Kit de développement Microsoft pour Java pour générer des classes pour ADO, celles-ci seront remplacées par les classes de l'Assistant Bibliothèque de types Java.

3.  Pour utiliser ces fichiers, ouvrez votre projet dans Visual J++. Dans le menu **Projet**, choisissez **Ajouter au projet**. Sélectionnez **des** fichiers et ajoutez tous les fichiers. Fichiers JAVA générés dans le \\ répertoire trustlib (par défaut c: \\ winnt java \\ \\ trustlib \\ msado15) pour votre projet.


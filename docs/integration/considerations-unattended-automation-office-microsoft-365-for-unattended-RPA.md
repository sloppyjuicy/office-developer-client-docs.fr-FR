---
title: Considérations relatives à l’automatisation sans assistance d’Office dans le Microsoft 365 pour un environnement de RPA sans assistance
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: Considérations relatives à l’automatisation sans assistance d’Office dans le Microsoft 365 pour un environnement de RPA sans assistance.
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103047"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Considérations relatives à l’automatisation sans assistance d’Office dans le Microsoft 365 pour un environnement de RPA sans assistance

Bien que Microsoft 365 pour les RPA sans assistance fournisse une licence qui permet l’automatisation d’Office sans aucun utilisateur, toutes les versions actuelles d’Office ont été conçues et testées pour s’exécuter en tant que produits utilisateur final sur une station de travail cliente, avec un utilisateur présent pour interagir avec l’interface de l’application. Les comportements inattendus résultant de l’utilisation d’applications sans utilisateur présent ne sont pas des défauts. Si vous souhaitez exécuter Office dans cette configuration, vous devez tenir compte de ces comportements inattendus dans votre logique d’application.

Cet article décrit certaines considérations relatives à l’automatisation sans assistance d’Office pour vous aider si vous utilisez cette approche. Toutefois, Notez que l’utilisation d’Office dans cette configuration est absolument « en l’espace » et doit tenir compte de ces comportements inattendus. Les informations fournies ici ne sont pas exhaustives et ne garantissent pas la résolution de tous les problèmes pour tous les clients. Nous vous encourageons à tester soigneusement votre solution avant de la déployer.

## <a name="common-problems-in-unattended-automation"></a>Problèmes courants dans l’automatisation sans assistance

Si vous souhaitez utiliser Office sans un utilisateur, gardez à l’esprit les domaines suivants dans lesquels Office peut se comporter différemment que prévu. Pour que votre solution s’exécute correctement, elle doit répondre à ces problèmes et réduire autant que possible leurs effets. Tenez compte de ces problèmes lorsque vous créez votre application.

### <a name="interactive-ui-elements"></a>Éléments d’interface utilisateur interactifs

Les applications Office partent du principe qu’elles sont exécutées de manière interactive. Si une erreur inattendue se produit, ou si un paramètre non spécifié est nécessaire pour effectuer une fonction, Office est conçu pour inviter l’utilisateur à saisir une boîte de dialogue demandant à l’utilisateur s’il souhaite continuer. Dans le cas d’une automatisation sans assistance, l’application peut apparaître comme « bloquée », car l’application s’arrête jusqu’à ce qu’elle reçoive cette entrée. Si vous automatisez Office via ses API publiques, vous pouvez supprimer un grand nombre de ces alertes en configurant les propriétés comme [application. DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) et [application. AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) de manière appropriée. Votre code doit être conçu pour identifier et traiter les alertes de blocage à tout moment.

### <a name="user-identity"></a>Identité de l’utilisateur

Les applications Office nécessitent une identité d’utilisateur lors de l’exécution des applications, même lorsque l’application est démarrée via Automation. Cette identité d’utilisateur peut entraîner un ou plusieurs des éléments suivants :

- La présence d’une interface utilisateur de connexion supplémentaire qui doit être gérée.
- Fichiers qui ne peuvent pas être ouverts ni modifiés en fonction des autorisations d’accès par utilisateur.
- Modifications inattendues des métadonnées du fichier (par exemple, certaines propriétés de fichier seront mises à jour en fonction de l’identité de l’utilisateur de l’instance de l’application automatisée).

Différentes approches peuvent vous aider à limiter ces problèmes ; par exemple, en exécutant l' [inspecteur de document](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) pour supprimer des métadonnées. Déterminez si ces approches sont appropriées en fonction de votre scénario.

### <a name="server-side-security"></a>Sécurité côté serveur

Lors de l’exécution d’Office sans assistance et du traitement de contenu de fichier arbitraire, aucune protection supplémentaire spécifique dans cet environnement n’est disponible pour empêcher le chargement et l’exécution des macros stockées dans ces fichiers. Office ne vous protège pas contre l’exécution involontaire de macros dans votre code ou depuis le démarrage d’un autre serveur qui peut exécuter des macros. Vous pouvez utiliser des propriétés comme [application. AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) pour atténuer ce risque, mais vous devez vous assurer que vous ne chargez que le contenu approuvé.

En outre, Office utilise un grand nombre de composants (tels que MAPI simple, WinInet et MSDAIPP) qui peuvent mettre en cache les informations d’authentification des clients pour accélérer le traitement. Quand Office est automatisé côté serveur et traite plusieurs fichiers, si les informations d’authentification ont été mises en cache pour cette session, un client peut utiliser les informations d’identification mises en cache d’un autre client. Par conséquent, le client peut obtenir des autorisations d’accès non octroyées en empruntant l’identité d’autres utilisateurs.

### <a name="ui-changes"></a>Modifications de l’interface utilisateur

Les éléments d’interface utilisateur dans Office sont largement stables, mais l’emplacement spécifique de n’importe quel élément d’interface utilisateur n’est pas garanti et peut changer à mesure que la conception de produit évolue pour incorporer les commentaires des utilisateurs et répondre aux besoins des clients. La logique de n’importe quelle automatisation doit en tenir compte. Ces modifications peuvent aboutir à des modifications de noms d’onglet de bouton ou de groupe, le déplacement de commandes entre les onglets, l’ajout de nouveaux onglets ou la suppression de commandes en alignement avec nos stratégies de désapprobation de fonctionnalités. Ces modifications peuvent avoir lieu dans l’interface utilisateur, ainsi que dans les informations d’accessibilité fournies par l’application, car ces informations sont modifiées afin d’améliorer la convivialité et de tenir compte des commentaires des clients, et peuvent être déployées pour différents utilisateurs à différents moments.

Même sans modification des produits, les différences entre les environnements système (tels que la taille/résolution de l’écran/PPP) peuvent entraîner des modifications dans l’emplacement des éléments à l’écran. Toute approche basée sur les coordonnées d’écran pour simuler l’entrée utilisateur doit tenir compte de ces modifications et s’adapter en conséquence.

### <a name="single-threading"></a>Monothreading

Les applications Office sont des applications STA, non réentrantes, conçues pour fournir des fonctionnalités variées et gourmandes en ressources pour un seul client. Les applications utilisent des ressources globales, telles que des fichiers mappés en mémoire, des modèles ou des compléments globaux, ainsi que des serveurs Automation partagés. Cela peut limiter le nombre d’instances pouvant être exécutées simultanément et conduire à des conditions de concurrence si les applications sont configurées dans un environnement multiclient. Si vous envisagez d’exécuter plusieurs instances d’une application Office, vous devez envisager de les isoler au niveau de la machine virtuelle afin de garantir la stabilité de la solution résultante.

### <a name="resiliency-and-stability"></a>Résistance et stabilité

Même avec les considérations ci-dessus, si les applications sont automatisées de manière à simuler une entrée utilisateur ou des longueurs de session qui dépassent considérablement l’utilisation interactive, ils peuvent rencontrer des problèmes qui ne sont pas présents lorsqu’ils sont exécutés de manière interactive. Les solutions qui utilisent Office dans ce contexte doivent créer de façon proactive des mécanismes pour surveiller l’état de l’application et les redémarrer (et/ou la machine virtuelle sur laquelle ils sont exécutés) si/le cas échéant.

## <a name="suggested-alternatives"></a>Alternatives suggérées

Microsoft recommande vivement quelques alternatives qui ne nécessitent pas l’installation d’Office et l’exécution côté serveur, et qui peuvent effectuer des tâches courantes de manière plus efficace et plus rapide que l’automatisation dans cette configuration. Avant d’impliquer Office en tant que composant côté serveur dans votre projet, envisagez d’autres solutions.

### <a name="microsoft-graph"></a>Microsoft Graph

L’API Microsoft Graph permet d’accéder aux services, données et informations d’aide disponibles pour les utilisateurs et les solutions dans le Cloud Microsoft, y compris de nombreux services prenant en charge les besoins de l’automatisation sans assistance : accès à la messagerie/calendrier/contacts/fichiers, conversion de documents, calcul de classeurs Excel, et bien plus encore. Ces services sont conçus pour une utilisation sans assistance et un accès à grande envergure, et utilisent une syntaxe d’API RESTful standard. Pour plus d’informations sur Microsoft Graph et sur la façon de l’utiliser pour manipuler les données des utilisateurs, consultez les rubriques suivantes :

- [Présentation de Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Prise en main de Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Télécharger un fichier dans un autre format](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) (conversion de fichier)
- [Utilisation d’Excel dans Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (Détails du classeur)

### <a name="open-xml-file-formats"></a>Formats de fichiers Open XML

De nombreuses tâches d’automatisation impliquent la création ou la modification de documents. Office prend en charge les formats de fichiers Open XML qui permettent aux développeurs de créer, modifier, lire et transformer du contenu de fichier à l’aide de technologies standard XML et ZIP, définies dans la norme internationale ISO 29500. Ces formats de fichiers peuvent être manipulés par le biais de n’importe quel outil ZIP/XML, y compris l’espace de noms System.IO.Package.IO dans l’infrastructure Microsoft .NET 3. x. La modification directe des formats de fichier est la méthode recommandée et prise en charge pour la gestion des modifications apportées aux fichiers Office à partir d’un service.

Microsoft fournit un kit de développement logiciel (SDK) pour manipuler les formats de fichiers Open XML à partir de l’infrastructure .NET 3. x. Pour plus d’informations sur le kit de développement logiciel (SDK) et sur l’utilisation du kit de développement logiciel (SDK) pour créer ou modifier des fichiers Open XML, consultez les rubriques suivantes :

- [Comprendre les formats de fichiers Open XML](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Bienvenue dans le kit de développement logiciel (SDK) Open XML 2,5 pour Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)

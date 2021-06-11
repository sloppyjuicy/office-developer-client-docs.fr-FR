---
title: Éléments à prendre en compte pour l’automatisation sans Office dans le Microsoft 365 pour un environnement RPA sans surveillance
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: Éléments à prendre en compte pour l’automatisation sans Office dans le Microsoft 365 pour un environnement RPA sans surveillance.
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103047"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Éléments à prendre en compte pour l’automatisation sans Office dans le Microsoft 365 pour un environnement RPA sans surveillance

Bien que Microsoft 365 pour la RPA sans surveillance fournit une licence qui permet l’automatisation de Office sans utilisateur présent, toutes les versions actuelles de Office ont été conçues et testées pour s’exécuter en tant que produits d’utilisateur final sur une station de travail cliente avec un utilisateur présent pour interagir avec l’interface de l’application. Les comportements inattendus résultant de l’utilisation d’applications sans utilisateur ne sont pas des défauts. Si vous souhaitez exécuter des Office dans cette configuration, vous devez être prêt à tenir compte de ces comportements inattendus dans la logique de votre application.

Cet article décrit quelques-unes des considérations à prendre en compte pour l’automatisation sans Office pour vous aider si vous utilisez cette approche. Toutefois, notez que l’utilisation des Office dans cette configuration est strictement « TELLE QU’ELLE » et doit tenir compte de ces comportements inattendus. Les informations fournies ici ne sont pas exhaustives et ne sont pas garanties pour résoudre tous les problèmes pour tous les clients. Nous vous encourageons à tester minutieusement votre solution avant de le déployer.

## <a name="common-problems-in-unattended-automation"></a>Problèmes courants dans l’automatisation sans surveillance

Si vous souhaitez utiliser Office sans utilisateur présent, n’ignorez pas les domaines dans lesquels les Office peuvent se comporter différemment que prévu. Pour que votre solution s’exécute correctement, elle doit résoudre ces problèmes et réduire autant que possible leurs effets. Examinez attentivement ces problèmes lorsque vous créez votre application.

### <a name="interactive-ui-elements"></a>Éléments d’interface utilisateur interactifs

Office applications supposent qu’elles sont en cours d’utilisation de manière interactive. Si une erreur inattendue se produit ou si un paramètre non spécifié est nécessaire pour terminer une fonction, Office est conçu pour demander à l’utilisateur une boîte de dialogue qui lui demande comment il souhaite continuer. Dans une automatisation sans surveillance, l’application peut apparaître comme « hang » lorsque l’application s’arrête jusqu’à ce qu’elle reçoit cette entrée. Si vous automatisez Office via ses API publiques, vous pouvez supprimer un grand nombre de ces alertes en configurant correctement des propriétés telles que [Application.DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) et [Application.AutomationSecurity.](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) Votre code doit être conçu pour identifier et traiter les alertes de blocage à tout moment.

### <a name="user-identity"></a>Identité de l’utilisateur

Office applications nécessitent une identité d’utilisateur lorsque les applications sont exécutés, même lorsque l’application est démarrée via automation. Cette identité d’utilisateur peut provoquer l’une ou l’ensemble des causes suivantes :

- Présence d’une interface utilisateur de sign-in supplémentaire qui doit être gérée.
- Fichiers qui ne peuvent pas être ouverts et/ou modifiés en fonction des autorisations d’accès par utilisateur.
- Modifications inattendues des métadonnées du fichier (par exemple, certaines propriétés du fichier seront mises à jour en fonction de l’identité de l’identité de l’utilisateur de l’instance d’application automatisée).

Diverses approches peuvent aider à atténuer ces problèmes ; par exemple, l’exécution de [l’Inspecteur de document](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) pour supprimer des métadonnées. Envisagez si ces approches sont appropriées en fonction de votre scénario.

### <a name="server-side-security"></a>Sécurité côté serveur

Lors de l’exécution Office sans surveillance et le traitement de contenu de fichier arbitraire, aucune protection supplémentaire spécifique à cet environnement n’est disponible pour empêcher le chargement et l’exécution des macros stockées dans ces fichiers. Office ne vous protège pas contre l’exécution involontaire de macros à partir de votre code ou le démarrage d’un autre serveur qui pourrait exécuter des macros. Vous pouvez utiliser des propriétés telles que [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) pour atténuer ce risque, mais vous devez vous assurer que vous chargez uniquement du contenu approuvé.

En outre, Office utilise de nombreux composants (tels que Simple MAPI, WinInet et MSDAIPP) qui peuvent mettre en cache les informations d’authentification client pour accélérer le traitement. Lorsque Office est automatisé côté serveur et traite plusieurs fichiers, si les informations d’authentification ont été mises en cache pour cette session, un client peut utiliser les informations d’identification mises en cache d’un autre client. Par conséquent, le client peut obtenir des autorisations d’accès non accordées en usurpant l’identité d’autres utilisateurs.

### <a name="ui-changes"></a>Modifications de l’interface utilisateur

Les éléments d’interface utilisateur dans Office sont en grande partie stables, mais l’emplacement spécifique d’un élément d’interface utilisateur n’est pas garanti et peut changer à mesure que la conception du produit évolue pour incorporer les commentaires des utilisateurs et répondre aux besoins des clients. La logique de toute automatisation doit en tenir compte. Ces modifications peuvent entraîner des modifications de nommage d’onglets de bouton ou de groupe, le déplacement de commandes entre les onglets, l’ajout de nouveaux onglets ou la suppression de commandes en alignement avec nos stratégies d’arrêt des fonctionnalités. Ces modifications peuvent avoir lieu dans l’interface utilisateur ainsi que dans les informations d’accessibilité fournies par l’application, car ces informations sont modifiées pour améliorer la facilité d’utilisation et tenir compte des commentaires des clients en cours et peuvent être déployées pour différents utilisateurs à différents moments.

Même sans modification du produit, les différences entre les environnements système (telles que la taille de l’écran/résolution/RÉSOLUTION) peuvent entraîner des modifications de l’emplacement des éléments à l’écran. Toute approche qui s’appuie sur les coordonnées de l’écran pour simuler l’entrée utilisateur doit prendre en compte ces modifications et s’adapter en conséquence.

### <a name="single-threading"></a>Thread unique

Office applications sont des applications non de réentrant, basées sur STA qui sont conçues pour fournir des fonctionnalités diverses mais qui font beaucoup de ressources pour un seul client. Les applications utilisent des ressources globales telles que des fichiers mappés à la mémoire, des modèles ou des add-ins globaux et des serveurs d’automatisation partagés. Cela peut limiter le nombre d’instances qui peuvent s’exécuter simultanément et entraîner des conditions de course si les applications sont configurées dans un environnement multiclient. Si vous prévoyez d’exécuter plusieurs instances d’une application Office, vous devez planifier de les isoler au niveau de la machine virtuelle pour garantir la stabilité de la solution résultante.

### <a name="resiliency-and-stability"></a>Résilience et stabilité

Même avec les considérations ci-dessus, si les applications sont automatisées de manière à simuler l’entrée utilisateur ou pour des durées de session qui dépassent considérablement l’utilisation interactive, elles peuvent rencontrer des problèmes qui ne sont pas présents lors de l’utilisation interactive. Les solutions qui utilisent Office dans ce contexte doivent créer de manière proactive des mécanismes pour surveiller l’état de l’application et les redémarrer (et/ou la machine virtuelle sur laquelle elles sont en cours d’exécution) si/si nécessaire.

## <a name="suggested-alternatives"></a>Alternatives suggérées

Microsoft recommande vivement quelques solutions qui ne nécessitent pas l’installation et l’utilisation de Office côté serveur, et qui peuvent effectuer des tâches courantes plus efficacement et plus rapidement que l’automatisation dans cette configuration. Avant d’Office en tant que composant côté serveur dans votre projet, envisagez d’autres solutions.

### <a name="microsoft-graph"></a>Microsoft Graph

L’API Microsoft Graph permet d’accéder aux services, données et renseignements disponibles pour les utilisateurs et solutions dans le cloud Microsoft, y compris de nombreux services qui permettent de répondre aux besoins de l’automatisation sans surveillance : accès à la messagerie/ calendrier/contacts/fichiers des utilisateurs, à la conversion de documents, au calcul d’un workbook Excel, etc. Ces services sont conçus pour une utilisation sans surveillance et un accès à grande échelle, et utilisent une syntaxe d’API RESTful standard. Pour plus d’informations sur Microsoft Graph et comment l’utiliser pour utiliser les données des utilisateurs, consultez les informations suivantes :

- [Présentation de Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Prise en main de Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Télécharger un fichier dans un autre format](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) (conversion de fichier)
- [Working with Excel in Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (workbook details)

### <a name="open-xml-file-formats"></a>Formats de fichiers Open XML

De nombreuses tâches d’automatisation impliquent la création ou la modification de documents. Office prend en charge les formats de fichiers Open XML qui permettent aux développeurs de créer, modifier, lire et transformer du contenu de fichier à l’aide des technologies XML et ZIP standard, définies dans la norme internationale ISO 29500. Ces formats de fichier peuvent être manipulés via n’importe quel outil ZIP/XML, y compris l’espace System.IO.Package.IO de noms dans Microsoft .NET 3.x Framework. La modification directe des formats de fichiers est la méthode recommandée et prise en charge pour gérer les modifications apportées Office fichiers à partir d’un service.

Microsoft fournit un SDK pour la manipulation des formats de fichier Open XML à partir de .NET 3.x Framework. Pour plus d’informations sur le SDK et sur l’utilisation du SDK pour créer ou modifier des fichiers Open XML, consultez les informations suivantes :

- [Comprendre les formats de fichiers Open XML](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Bienvenue dans le SDK Open XML 2.5 pour Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)

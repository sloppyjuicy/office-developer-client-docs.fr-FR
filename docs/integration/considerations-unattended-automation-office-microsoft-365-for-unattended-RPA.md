---
title: Considérations relatives à l’automatisation sans assistance des Office dans le Microsoft 365 pour l’environnement RPA sans assistance
ms.date: 03/30/2020
ms.audience: Developer
ms.localizationpriority: medium
description: Considérations relatives à l’automatisation sans assistance des Office dans le Microsoft 365 pour l’environnement RPA sans assistance.
ms.openlocfilehash: b920e5f589547dd4a20c45b622d1268dda8e1266
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65771089"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Considérations relatives à l’automatisation sans assistance des Office dans le Microsoft 365 pour l’environnement RPA sans assistance

Bien que Microsoft 365 pour RPA sans assistance fournit une licence qui permet l’automatisation de Office sans utilisateur présent, toutes les versions actuelles de Office ont été conçues et testées pour s’exécuter en tant que produits d’utilisateur final sur une station de travail cliente avec un utilisateur présent pour interagir avec l’interface de l’application. Les comportements inattendus résultant de l’utilisation d’applications sans l’intervention d’un utilisateur ne sont pas des défauts. Si vous souhaitez exécuter Office dans cette configuration, vous devez être prêt à prendre en compte ces comportements inattendus dans votre logique d’application.

Cet article décrit certaines des considérations relatives à l’automatisation sans assistance de Office pour vous aider si vous utilisez cette approche. Toutefois, notez que l’utilisation de Office dans cette configuration est strictement « AS IS » et doit tenir compte de ces comportements inattendus. Les informations fournies ici ne sont pas exhaustives et ne sont pas garanties pour résoudre tous les problèmes pour tous les clients. Nous vous encourageons à tester soigneusement votre solution avant de procéder au déploiement.

## <a name="common-problems-in-unattended-automation"></a>Problèmes courants dans l’automatisation sans assistance

Si vous souhaitez utiliser Office sans qu’un utilisateur soit présent, tenez compte des domaines suivants dans lesquels Office peuvent se comporter différemment de ce qui était prévu. Pour que votre solution s’exécute correctement, elle doit résoudre ces problèmes et réduire autant que possible leurs effets. Tenez compte de ces problèmes avec soin lorsque vous générez votre application.

### <a name="interactive-ui-elements"></a>Éléments d’interface utilisateur interactifs

Office applications supposent qu’elles sont exécutées de manière interactive. Si une erreur inattendue se produit, ou si un paramètre non spécifié est nécessaire pour effectuer une fonction, Office est conçu pour inviter l’utilisateur avec une boîte de dialogue qui demande à l’utilisateur comment il souhaite continuer. Dans le cadre d’une automatisation sans assistance, l’application peut apparaître comme « bloquée » à mesure que l’application s’arrête jusqu’à ce qu’elle reçoive cette entrée. Si vous automatisez Office via ses API publiques, vous pouvez supprimer un grand nombre de ces alertes en configurant des propriétés comme [Application.DisplayAlerts](/office/vba/api/word.application.displayalerts) et [Application.AutomationSecurity](/office/vba/api/word.application.automationsecurity) de manière appropriée. Votre code doit être conçu pour identifier et traiter les alertes bloquantes à tout moment.

### <a name="user-identity"></a>Identité de l’utilisateur

Office applications nécessitent une identité d’utilisateur lorsque les applications sont exécutées, même lorsque l’application est démarrée via l’automatisation. Cette identité d’utilisateur peut provoquer l’une ou l’autre des opérations suivantes :

- Présence d’une interface utilisateur de connexion supplémentaire qui doit être gérée.
- Fichiers qui ne peuvent pas être ouverts et/ou modifiés en fonction des autorisations d’accès par utilisateur.
- Modifications inattendues apportées aux métadonnées du fichier (par exemple, certaines propriétés de fichier seront mises à jour en fonction de l’identité de l’identité utilisateur de l’instance d’application automatisée).

Diverses approches peuvent aider à atténuer ces problèmes; par exemple, l’exécution de [l’Inspecteur de document](/office/vba/library-reference/concepts/using-the-document-inspector) pour supprimer les métadonnées. Déterminez si ces approches sont appropriées en fonction de votre scénario.

### <a name="server-side-security"></a>Sécurité côté serveur

Lors de l’exécution Office contenu de fichier arbitraire sans assistance et de traitement, aucune protection supplémentaire spécifique dans cet environnement n’est disponible pour empêcher le chargement et l’exécution des macros stockées dans ces fichiers. Office ne vous protège pas contre l’exécution involontaire de macros à partir de votre code ou le démarrage d’un autre serveur susceptible d’exécuter des macros. Vous pouvez utiliser des propriétés comme [Application.AutomationSecurity](/office/vba/api/word.application.automationsecurity) pour atténuer ce risque, mais vous devez vous assurer que vous chargez uniquement du contenu approuvé.

En outre, Office utilise de nombreux composants (tels que Simple MAPI, WinInet et MSDAIPP) qui peuvent mettre en cache les informations d’authentification du client pour accélérer le traitement. Lorsque Office est automatisé côté serveur et traite plusieurs fichiers, si les informations d’authentification ont été mises en cache pour cette session, un client peut utiliser les informations d’identification mises en cache d’un autre client. Par conséquent, le client peut obtenir des autorisations d’accès non accordées en empruntant l’identité d’autres utilisateurs.

### <a name="ui-changes"></a>Modifications de l’interface utilisateur

Les éléments d’interface utilisateur dans Office sont en grande partie stables, mais l’emplacement spécifique d’un élément d’interface utilisateur n’est pas garanti et peut changer à mesure que la conception du produit évolue pour incorporer les commentaires des utilisateurs et répondre aux besoins des clients. La logique de toute automatisation doit en tenir compte. Ces modifications peuvent entraîner des modifications de nommage des onglets de bouton ou de groupe, le déplacement des commandes entre les onglets, l’ajout de nouveaux onglets ou la suppression de commandes alignées sur nos stratégies de dépréciation des fonctionnalités. Ces modifications peuvent avoir lieu dans l’interface utilisateur ainsi que dans les informations d’accessibilité fournies par l’application, car ces informations sont modifiées pour améliorer la convivialité et tenir compte des commentaires continus des clients, et peuvent être déployées pour différents utilisateurs à différents moments.

Même sans modification du produit, les différences entre les environnements système (par exemple, taille d’écran/résolution/PPP) peuvent entraîner des modifications de l’emplacement des éléments à l’écran. Toute approche qui s’appuie sur des coordonnées d’écran pour simuler l’entrée utilisateur doit prendre en compte ces modifications et s’adapter en conséquence.

### <a name="single-threading"></a>Monothreading

Office applications sont des applications non réentrantes basées sur STA qui sont conçues pour fournir des fonctionnalités variées mais gourmandes en ressources pour un seul client. Les applications utilisent des ressources globales telles que des fichiers mappés en mémoire, des compléments ou des modèles globaux et des serveurs Automation partagés. Cela peut limiter le nombre d’instances pouvant s’exécuter simultanément et entraîner des conditions de concurrence si les applications sont configurées dans un environnement multiclient. Si vous envisagez d’exécuter plusieurs instances d’une application Office, vous devez les isoler au niveau de la machine virtuelle pour garantir la stabilité de la solution résultante.

### <a name="resiliency-and-stability"></a>Résilience et stabilité

Même avec les considérations ci-dessus, si les applications sont automatisées de manière à simuler l’entrée utilisateur ou pour les longueurs de session qui dépassent considérablement l’utilisation interactive, elles peuvent rencontrer des problèmes qui ne sont pas présents lors de l’exécution interactive. Les solutions qui utilisent Office dans ce contexte doivent créer de manière proactive des mécanismes pour surveiller l’état de l’application et les redémarrer (et/ou la machine virtuelle sur laquelle elles s’exécutent) si nécessaire.

## <a name="suggested-alternatives"></a>Alternatives suggérées

Microsoft recommande vivement quelques alternatives qui ne nécessitent pas l’installation et l’exécution de Office côté serveur, et qui peuvent effectuer des tâches courantes plus efficacement et plus rapidement que l’automatisation dans cette configuration. Avant d’impliquer Office en tant que composant côté serveur dans votre projet, envisagez d’autres solutions.

### <a name="microsoft-graph"></a>Microsoft Graph

Microsoft API Graph fournit l’accès aux services, aux données et à l’intelligence qui sont disponibles pour les utilisateurs et les solutions dans le cadre du cloud Microsoft, y compris de nombreux services qui prennent en charge les besoins de l’automatisation sans assistance : accès à la messagerie/ calendrier/contacts/fichiers des utilisateurs, conversion de documents, calcul Excel classeur, etc. Ces services sont conçus pour une utilisation sans assistance et un accès à grande échelle, et utilisent une syntaxe d’API RESTful standard. Pour plus d’informations sur Microsoft Graph et son utilisation pour utiliser les données des utilisateurs, consultez les rubriques suivantes :

- [Présentation de Microsoft Graph](/graph/overview) 
- [Prise en main de Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Télécharger un fichier dans un autre format](/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http&preserve-view=true) (conversion de fichier)
- [Utilisation de Excel dans Microsoft Graph](/graph/api/resources/excel) (détails du classeur)

### <a name="open-xml-file-formats"></a>Ouvrir des formats de fichier XML

De nombreuses tâches d’automatisation impliquent la création ou la modification de documents. Office prend en charge les formats de fichiers Open XML qui permettent aux développeurs de créer, modifier, lire et transformer du contenu de fichiers à l’aide des technologies XML et ZIP standard, définies dans la norme internationale ISO 29500. Ces formats de fichier peuvent être manipulés via n’importe quel outil ZIP/XML, y compris l’espace de noms System.IO.Package.IO dans Microsoft .NET 3.x Framework. La modification directe des formats de fichier est la méthode recommandée et prise en charge pour gérer les modifications apportées aux fichiers Office à partir d’un service.

Microsoft fournit un Kit de développement logiciel (SDK) pour manipuler les formats de fichiers Open XML à partir du .NET 3.x Framework. Pour plus d’informations sur le Kit de développement logiciel (SDK) et sur l’utilisation du Kit de développement logiciel (SDK) pour créer ou modifier des fichiers Open XML, consultez les rubriques suivantes :

- [Comprendre les formats de fichiers Open XML](/office/open-xml/understanding-the-open-xml-file-formats)
- [Bienvenue dans le Kit de développement logiciel (SDK) Open XML 2.5 pour Office](/office/open-xml/open-xml-sdk)

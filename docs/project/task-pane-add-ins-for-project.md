---
title: Compléments du volet Office pour Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 et Project Professionnel 2013 2013 prise en charge des Office de volet des tâches. Vous pouvez utiliser des applications de volet de tâches pour intégrer des données de projet, de tâche, de ressource et d’affichage dans un projet à d’autres applications clientes Office 2013, applications SharePoint, composants WebPart, autres pages web et données externes.
ms.openlocfilehash: 85957e303ef49eb75d86dc5d35604f4dcc5d07ed
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180550"
---
# <a name="task-pane-add-ins-for-project"></a>Compléments du volet Office pour Project

Project Standard 2013 et Project Professionnel 2013 2013 prise en charge des Office de volet des tâches. Vous pouvez utiliser des applications de volet de tâches pour intégrer des données de projet, de tâche, de ressource et d’affichage dans un projet à d’autres applications clientes Office 2013, applications SharePoint, composants WebPart, autres pages web et données externes.
  
Office les applications sont un modèle d’extensibilité pris en charge dans Office applications clientes 2013. La plateforme complète du add-in inclut des types de modules de recherche contextuels, de contenu et de volet de tâches. Outlook 2013 prend en charge les modules de messagerie, qui peuvent afficher une page web dans un message électronique ou un élément de rendez-vous de calendrier lié au contenu de l’élément. Word 2013 et Excel 2013 peuvent prendre en charge les applications de contenu, qui peuvent afficher une page web en tant que contenu incorporé dans un document. Word 2013, Excel 2013 et Project Professionnel 2013 prendre en charge les applications du volet Des tâches, qui peuvent afficher une page web dans un volet De tâches où le contenu est lié aux informations contextuelles dans le projet.
  
Par exemple, un complément Project peut résumer les données du projet actif et afficher des données supplémentaires sur une tâche ou une ressource sélectionnée. Les données associées dans le add-in peuvent être provenant d’une source externe telle qu’une liste SharePoint, des tables de création de rapports dans la base de données Project Server, un service web ou une autre application d’entreprise. Un add-in du volet Des tâches peut être développé avec HTML 5, JavaScript, JQuery et d’autres bibliothèques JavaScript. Un add-in du volet Des tâches ne prend pas directement en charge ActiveX composants Flash, Silverlight ou Silverlight. Bien qu’un Office puisse utiliser un élément **IFrame** pour accéder à une application web côté serveur qui utilise ASP.NET et la bibliothèque .NET Framework 4.5, ce type de solution n’est ni recommandé ni pris en charge. Le add-in peut être développé pour enregistrer les données localement ou écrire des données à un emplacement externe. 
  
> [!NOTE]
> Le volet Des tâches Project les applications peuvent accéder aux données à partir Project Online l’authentification OAuth. Avec Project Professionnel 2013, vous pouvez développer des add-ins du volet Des tâches qui accèdent aux installations sur site de Project Server 2013 et aux SharePoint 2013 sur site ou en ligne. Par exemple, voir [Connexion d’un Project](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) du volet Des tâches à PWA dans le blog Project programmibilité. > Project Standard 2013 ne prend pas en charge l’intégration directe avec les données Project Server ou les listes de tâches SharePoint synchronisées avec Project Server. 
  
Pour plus d’informations sur les Office 2013, voir Office [et SharePoint des modules complémentaires.](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29) 
  
## <a name="developing-task-pane-add-ins"></a>Développement de add-ins de volet de tâches

La documentation pour les développeurs Office et SharePoint de développement inclut des articles complets et des références. Pour obtenir une présentation du développement de add-ins pour Project Professionnel 2013 et d’autres applications clientes Office 2013, ainsi que pour la référence JavaScript et la référence de manifeste XML, voir [Office Add-ins](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29).
  
Le téléchargement du SDK Project 2013 inclut l’exemple de add-in **test** du modèle modèle Project qui montre comment obtenir le GUID d’une tâche, d’une ressource et d’une vue, comment obtenir les propriétés du projet actif et comment définir un handleur d’événements modifié de sélection de tâche, de ressource ou d’affichage. Lorsque vous extrayez et installez le SDK et les exemples dans le fichier Project2013SDK.msi, consultez le sous-dossier et  `\Samples\Apps\Copy_to_AppSource_FileShare`  `\Samples\Apps\Copy_to_AppManifests_FileShare` le sous-dossier. LJSOMCall.html exemple utilise les fonctions JavaScript dans le fichier office.js et le fichier project-15.js, qui sont inclus dans le téléchargement. Vous pouvez utiliser les fichiers de débogage correspondants (office.debug.js et project-15.debug.js) pour examiner les fonctions. 
  
**L HelloProject_OData** exemple de Project Professionnel 2013 a été développé avec Visual Studio 2012. Le add-in utilise une requête REST du service **ProjectData** pour obtenir des données de rapport pour le coût du projet et d’autres informations, puis compare le projet actuel avec les valeurs moyennes de tous les projets dans Project Web App. 
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Compléments du volet Office pour Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Connexion d’Project de volet de tâches à un PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Téléchargement du kit de développement logiciel (SDK) de Project 2013](https://www.microsoft.com/download/details.aspx?id=30435%20)
    
- [Compléments Office et SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Compléments Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    


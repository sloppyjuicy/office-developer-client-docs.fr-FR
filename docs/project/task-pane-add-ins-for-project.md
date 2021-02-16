---
title: Compléments du volet Office pour Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 et Project Professional 2013 sont tous deux en charge des add-ins Office du volet Office. Vous pouvez utiliser des applications du volet Office pour intégrer des données de projet, de tâche, de ressource et d’affichage dans un projet avec d’autres applications clientes Office 2013, des applications SharePoint, des WebParts, d’autres pages web et des données externes.
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330015"
---
# <a name="task-pane-add-ins-for-project"></a>Compléments du volet Office pour Project

Project Standard 2013 et Project Professional 2013 sont tous deux en charge des add-ins Office du volet Office. Vous pouvez utiliser des applications du volet Office pour intégrer des données de projet, de tâche, de ressource et d’affichage dans un projet avec d’autres applications clientes Office 2013, des applications SharePoint, des WebParts, d’autres pages web et des données externes.
  
Les applications office sont un modèle d’extensibilité pris en charge dans plusieurs applications clientes Office 2013. La plateforme complète du add-in inclut des types de modules de recherche contextuels, de contenu et de volet de tâches. Outlook 2013 prend en charge les modules de messagerie, qui peuvent afficher une page web dans un message électronique ou un élément de rendez-vous de calendrier lié au contenu de l’élément. Word 2013 et Excel 2013 prendre en charge les applications de contenu, qui peuvent afficher une page web en tant que contenu incorporé dans un document. Word 2013, Excel 2013 et Project Professionnel 2013 prendre en charge les modules complémentaires du volet Des tâches, qui peuvent afficher une page web dans un volet De tâches où le contenu est lié aux informations contextuelles dans le projet.
  
Par exemple, un complément Project peut résumer les données du projet actif et afficher des données supplémentaires sur une tâche ou une ressource sélectionnée. Les données associées dans le add-in peuvent être provenant d’une source externe telle qu’une liste SharePoint, des tables de création de rapports dans la base de données Project Server, un service web ou une autre application d’entreprise. Un add-in du volet Des tâches peut être développé avec HTML 5, JavaScript, JQuery et d’autres bibliothèques JavaScript. Un add-in du volet Des tâches ne prend pas directement en charge ActiveX composants Flash, Silverlight ou Silverlight. Bien qu’un add-in Office puisse utiliser un élément **IFrame** pour accéder à une application web côté serveur qui utilise ASP.NET et la bibliothèque .NET Framework 4.5, ce type de solution n’est ni recommandé ni pris en charge. Le add-in peut être développé pour enregistrer les données localement ou écrire des données à un emplacement externe. 
  
> [!NOTE]
> Les applications Project du volet De tâches peuvent accéder aux données à partir de Project Online à l’aide de l’authentification OAuth. Avec Project Professionnel 2013, vous pouvez développer des add-ins du volet Des tâches qui accèdent à la fois aux installations sur site de Project Server 2013 et à SharePoint 2013 en local ou en ligne. Par exemple, voir [Connexion d’un add-in](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) du volet Office project à PWA dans le blog programmibility de Project. > Project Standard 2013 ne prend pas en charge l’intégration directe avec les données Project Server ou les listes de tâches SharePoint synchronisées avec Project Server. 
  
Pour plus d’informations sur les add-ins pour Office 2013, consultez [les add-ins Office et SharePoint.](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29) 
  
## <a name="developing-task-pane-add-ins"></a>Développement de add-ins de volet de tâches

La documentation pour les développeurs pour les applications Office et SharePoint inclut des articles complets et des références. Pour une introduction au développement de add-ins pour Project Professionnel 2013 et d’autres applications clientes Office 2013, ainsi que pour la référence JavaScript et la référence de manifeste XML, voir Les [add-ins Office.](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
  
Le téléchargement du SDK Project 2013 inclut l’exemple de add-in Test du modèle modèle de **Project** qui montre comment obtenir le GUID d’une tâche, d’une ressource et d’une vue, comment obtenir les propriétés du projet actif et comment définir un handler d’événement modifié de sélection de tâche, de ressource ou d’affichage. Lorsque vous extrayez et installez le SDK et les exemples dans le fichier Project2013SDK.msi, consultez le sous-dossier et  `\Samples\Apps\Copy_to_AppSource_FileShare`  `\Samples\Apps\Copy_to_AppManifests_FileShare` le sous-dossier. LJSOMCall.html utilise des fonctions JavaScript dans le fichier office.js et le fichier project-15.js, qui sont inclus dans le téléchargement. Vous pouvez utiliser les fichiers de débogage correspondants (office.debug.js et project-15.debug.js) pour examiner les fonctions. 
  
**L HelloProject_OData** exemple de add-in pour Project Professionnel 2013 a été développé avec Visual Studio 2012. Le add-in utilise une requête REST du service **ProjectData** pour obtenir des données de rapport pour le coût du projet et d’autres informations, puis compare le projet actuel avec les valeurs moyennes de tous les projets dans Project Web App. 
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Compléments du volet Office pour Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Connexion d’un add-in du volet Office Project à PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Téléchargement du Kit de développement logiciel (SDK) de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Compléments Office et SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Compléments Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    


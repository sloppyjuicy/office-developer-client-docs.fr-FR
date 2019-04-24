---
title: Compléments du volet Office pour Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project standard 2013 et Project Professional 2013 prennent tous deux en charge les compléments Office de volet de tâches. Vous pouvez utiliser des compléments du volet Office pour intégrer les données de projet, de tâche, de ressource et d'affichage dans un projet avec d'autres applications clientes Office 2013, des applications SharePoint, des composants WebPart, d'autres pages Web et des données externes.
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330015"
---
# <a name="task-pane-add-ins-for-project"></a>Compléments du volet Office pour Project

Project standard 2013 et Project Professional 2013 prennent tous deux en charge les compléments Office de volet de tâches. Vous pouvez utiliser des compléments du volet Office pour intégrer les données de projet, de tâche, de ressource et d'affichage dans un projet avec d'autres applications clientes Office 2013, des applications SharePoint, des composants WebPart, d'autres pages Web et des données externes.
  
Les compléments Office sont un modèle d'extensibilité pris en charge dans plusieurs applications clientes Office 2013. La plateforme de complément complète inclut des types de compléments contextuels, de contenu et de volet de tâches. Outlook 2013 prend en charge les compléments de messagerie, qui peuvent afficher une page Web dans un message électronique ou un élément de rendez-vous de calendrier qui est lié au contenu de l'élément. Word 2013 et Excel 2013 prennent en charge les compléments de contenu, qui peuvent afficher une page Web sous la forme d'un contenu incorporé dans un document. Les compléments de volet Office pour Word 2013, Excel 2013 et Project Professionnel 2013, qui peuvent afficher une page Web dans un volet Office dans lequel le contenu est lié à des informations contextuelles au sein du projet.
  
Par exemple, un complément Project peut synthétiser les données du projet actif et afficher des données supplémentaires sur une tâche ou une ressource sélectionnée. Les données connexes dans le complément peuvent provenir d'une source externe telle qu'une liste SharePoint, des tables de création de rapports dans la base de données Project Server, un service Web ou une autre application d'entreprise. Un complément de volet de tâches peut être développé avec HTML 5, JavaScript, JQuery et d'autres bibliothèques JavaScript. Un complément du volet Office ne prend pas directement en charge les composants ActiveX, Silverlight ou Flash. Bien qu'un complément Office puisse utiliser un élément **IFRAME** pour accéder à une application Web côté serveur qui utilise ASP.net et la bibliothèque .net Framework 4,5, ce type de solution n'est ni recommandé ni pris en charge. Le complément peut être développé pour enregistrer les données localement ou écrire des données dans un emplacement externe. 
  
> [!NOTE]
> Les compléments de projet de volet de tâches peuvent accéder aux données à partir de Project Online à l'aide de l'authentification OAuth. Avec Project Professionnel 2013, vous pouvez développer des compléments de volet de tâches qui accèdent à des installations locales de Project Server 2013 et de SharePoint 2013 sur site ou en ligne. Par exemple, reportez-vous à la rubrique [Connecting a Project Task Pane Add-in PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) dans le blog Project Programmibility. > Project standard 2013 ne prend pas en charge l'intégration directe avec des données Project Server ou des listes de tâches SharePoint synchronisées avec Project Server. 
  
Pour plus d'informations sur les compléments pour Office 2013, reportez-vous à la rubrique [Compléments Office et SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Développement de compléments de volet de tâches

La documentation destinée aux développeurs pour les compléments Office et SharePoint comprend des articles et des références complets. Pour une introduction au développement de compléments pour Project Professionnel 2013 et d'autres applications clientes Office 2013, ainsi que pour la référence JavaScript et la référence de manifeste XML, consultez la rubrique [Compléments Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29).
  
Le téléchargement du kit de développement logiciel (SDK) Project 2013 inclut l'exemple de complément **test Project OM** qui montre comment obtenir le GUID d'une tâche, d'une ressource et d'un affichage, comment obtenir les propriétés du projet actif et comment définir une tâche, une ressource ou un gestionnaire d'événements de modification de la sélection. Lorsque vous extrayez et installez le kit de développement logiciel (SDK) et les exemples `\Samples\Apps\Copy_to_AppSource_FileShare` dans le fichier Project2013SDK. `\Samples\Apps\Copy_to_AppManifests_FileShare` MSI, consultez le sous-répertoire et le sous-répertoire. L'exemple JSOMCall. html utilise des fonctions JavaScript dans le fichier Office. js et le fichier Project-15. js, qui sont inclus dans le téléchargement. Vous pouvez utiliser les fichiers de débogage correspondants (office.debug.js et project-15.debug.js) pour examiner les fonctions. 
  
Le complément **HelloProject_OData** Sample pour Project Professional 2013 a été développé avec Visual Studio 2012. Le complément utilise une requête REST du service **ProjectData** pour obtenir des données de rapport sur le coût du projet et d'autres informations, puis compare le projet actuel avec les valeurs moyennes de tous les projets dans Project Web App. 
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Compléments du volet Office pour Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Connexion d'un complément du volet Office Project à PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Téléchargement du Kit de développement logiciel (SDK) de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Compléments Office et SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Compléments Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    


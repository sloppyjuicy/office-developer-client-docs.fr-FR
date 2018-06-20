---
title: Compléments du volet Office pour Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 et Project Professional 2013 volet Office Add-ins prennent en charge. Vous pouvez utiliser des compléments de volet de tâches pour intégrer des projets, tâches, ressources et afficher les données dans un projet avec les autres applications clientes Office 2013, les applications SharePoint, les composants WebPart, autres pages Web et les données externes.
ms.openlocfilehash: 1432f38e9f2c87b7d5d33500d958222b2c15d7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787929"
---
# <a name="task-pane-add-ins-for-project"></a>Compléments du volet Office pour Project

Project Standard 2013 et Project Professional 2013 volet Office Add-ins prennent en charge. Vous pouvez utiliser des compléments de volet de tâches pour intégrer des projets, tâches, ressources et afficher les données dans un projet avec les autres applications clientes Office 2013, les applications SharePoint, les composants WebPart, autres pages Web et les données externes.
  
Compléments Office est un modèle d’extensibilité qui est pris en charge dans plusieurs applications de client Office 2013. La plateforme complète complément inclut contextuelle, contenu et types de complément de volet de tâches. Outlook 2013 prend en charge la messagerie des compléments, qui peuvent afficher une page Web dans un message électronique ou rendez-vous de calendrier qui est lié au contenu de l’élément. Word 2013 and Excel 2013 prend en charge le contenu des compléments, qui peuvent afficher une page Web en tant que contenu incorporé dans un document. Word 2013, Excel 2013 et Project Professional 2013 prend en charge la tâche volet compléments, qui peuvent afficher une page Web dans un volet Office dans laquelle le contenu est lié à des informations contextuelles dans le projet.
  
Par exemple, un projet complément peut synthétiser les données dans le projet actif et afficher des données supplémentaires sur une tâche ou ressource sélectionnée. Les données associées dans le complément peuvent provenir d’une source externe, telle qu’une liste SharePoint, rapports de tableaux dans la base de données Project Server, un service web ou une autre application d’entreprise. Un complément volet de tâches peut être développé de 5 HTML, JavaScript, JQuery et autres bibliothèques JavaScript. Un complément de volet Office ne prend pas directement en charge ActiveX, Silverlight ou composants Flash. Bien qu’un complément Office peut utiliser un élément **IFrame** pour accéder à une application web côté serveur qui utilise ASP.NET et la bibliothèque de .NET Framework 4.5, ce type de solution n’est pas recommandé ou pris en charge. Le complément peut être développé pour enregistrer les données localement ou écrire des données dans un emplacement externe. 
  
> [!NOTE]
> Volet Office Project compléments permettre accéder aux données à partir de Project Online à l’aide de l’authentification OAuth. Avec Project Professional 2013, vous pouvez développer la tâche volet compléments qui accèdent à ces deux installations locales de Project Server 2013 et sur site ou en ligne SharePoint 2013. Par exemple, voir [connexion d’un volet de tâches de projet complément dans PWA](http://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) dans le blog Project Programmibility. > Project Standard 2013 ne prend pas en charge l’intégration directe aux données Project Server ou des listes de tâches SharePoint qui sont synchronisés avec Project Server. 
  
Pour plus d’informations sur les compléments pour Office 2013, voir [Office et SharePoint Add-ins](http://msdn.microsoft.com/en-us/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Développement de compléments de volet de tâches

La documentation du développeur pour Office et SharePoint Add-ins inclut des références et des articles complètes. Pour obtenir une introduction au développement de compléments pour Project Professional 2013 et les autres applications clientes Office 2013 et pour la référence JavaScript et la référence du manifeste XML, voir les [compléments Office](http://msdn.microsoft.com/en-us/library/office/apps/jj220060%28v=office.15%29).
  
Le téléchargement du Kit de développement Project 2013 inclut le **Test du modèle objet Project** exemple complément qui montre comment obtenir le GUID de tâche, de ressource et d’affichage, comment obtenir les propriétés du projet actif et comment définir une tâche, une ressource ou afficher le Gestionnaire d’événements de changement de sélection. Lorsque vous extrayez et installez le Kit de développement logiciel et exemples dans le fichier Project2013SDK.msi, consultez le `\Samples\Apps\Copy_to_AppSource_FileShare` sous-répertoire et `\Samples\Apps\Copy_to_AppManifests_FileShare` sous-répertoire. L’exemple JSOMCall.html utilise les fonctions JavaScript dans le fichier office.js et le fichier project-15.js, qui sont inclus dans le téléchargement. Vous pouvez utiliser les fichiers de débogage correspondants (office.debug.js et project-15.debug.js) pour examiner les fonctions. 
  
Le complément exemple de **HelloProject_OData** pour Project Professional 2013 a été développé avec Visual Studio 2012. Le complément utilise une requête REST du service **ProjectData** pour obtenir les données de coût de projet et d’autres informations rapports, puis compare le projet actuel avec les valeurs moyennes de tous les projets dans Project Web App. 
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Compléments du volet Office pour Project](http://msdn.microsoft.com/en-us/library/office/apps/fp161143%28v=office.15%29)
    
- [Connexion d’un volet de tâches de projet de complément à PWA](http://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Téléchargement du Kit de développement logiciel (SDK) de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Office et SharePoint Add-ins](http://msdn.microsoft.com/en-us/library/office/fp161507%28v=office.15%29)
    
- [Compléments Office](http://msdn.microsoft.com/en-us/library/office/apps/jj220060%28v=office.15%29)
    


---
title: Énumérations (référence du développeur OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: Cette rubrique décrit les énumérations dans le modèle d’objet OneNote 2013.
ms.openlocfilehash: ccd75843326ea5942aa80d02246e59e92331a7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782532"
---
# <a name="enumerations-onenote-developer-reference"></a>Énumérations (référence du développeur OneNote)

Cette rubrique décrit les énumérations dans le modèle d’objet OneNote 2013.
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

Lorsqu’il est passé à la méthode **OpenHierarchy** , spécifie le type d’objet à créer, si, si le chemin d’accès passé à la méthode n’existe pas encore. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**cftNone** <br/> |0  <br/> |Ne crée aucun nouvel objet.  <br/> |
|**cftNotebook** <br/> |1  <br/> |Crée un bloc-notes en utilisant le nom spécifié et l’emplacement.  <br/> |
|**cftFolder** <br/> |2  <br/> |Crée un groupe de la section en utilisant le nom spécifié et l’emplacement.  <br/> |
|**cftSection** <br/> |3  <br/> |Crée une section en utilisant le nom spécifié et l’emplacement.  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Indique l’emplacement d’une fenêtre OneNote 2013 ancrée à l’aide de l’interface de la [fenêtre](window-interfaces-onenote.md) . S’il l' **DockedLocation** propriété, spécifie l’emplacement auquel ancrer une fenêtre OneNote. Cette énumération est nouvelle dans OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |La fenêtre OneNote est ancrée à l’emplacement par défaut sur le bureau.  <br/> |
|**dlLeft** <br/> |1  <br/> |La fenêtre OneNote est ancrée sur le côté gauche du bureau.  <br/> |
|**dlRight** <br/> |2  <br/> |La fenêtre OneNote est ancrée sur le côté droit du bureau.  <br/> |
|**dlTop** <br/> |3  <br/> |La fenêtre OneNote est ancrée dans la partie supérieure du bureau.  <br/> |
|**dlBottom** <br/> |4  <br/> |La fenêtre OneNote est ancrée au bas du bureau.  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

Lorsqu’il est passé à la méthode **SetFilingLocation** , spécifie le type de contenu l’emplacement de la classification est définie pour lorsque le type de contenu est envoyé à OneNote. Cette énumération est nouvelle dans OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**flEMail** <br/> |0  <br/> |Définit si les messages électroniques Outlook seront présentés.  <br/> |
|**flContacts** <br/> |1  <br/> |Définit si les contacts Outlook seront présentées.  <br/> |
|**flTasks** <br/> |2  <br/> |Définit si les tâches Outlook seront présentées.  <br/> |
|**flMeetings** <br/> |3  <br/> |Définit si les réunions Outlook seront présentées.  <br/> |
|**flWebContent** <br/> |4  <br/> |Définit où est classées contenu Internet Explorer.  <br/> |
|**flPrintOuts** <br/> |5  <br/> |Définit si les documents imprimés à partir de l’imprimante OneNote seront présentées.  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

Lorsqu’il est passé à la méthode **SetFilingLocation** , spécifie si le contenu qui est envoyé à OneNote est présentée. Cette énumération est nouvelle dans OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |0  <br/> |Définit le contenu à être archivé sur une nouvelle page dans une section spécifiée.  <br/> |
|**fltCurrentSectionNewPage** <br/> |1  <br/> |Définit le contenu à être archivé sur une nouvelle page dans la section active.  <br/> |
|**fltCurrentPage** <br/> |2  <br/> |Définit le contenu à la page active.  <br/> |
|**fltNamedPage** <br/> |4  <br/> |Définit le contenu être déposée dans une page spécifiée.  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

Lorsque affecté à la propriété **TreeDepth** de l’interface [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md) , spécifie la profondeur de l’arborescence de OneNote à afficher lorsque la boîte de dialogue Remplissage rapide s’affiche. Lorsqu’il est passé à la méthode **AddButton** de l’objet **IQuickFilingDialog** , fait référence à certains éléments de la hiérarchie OneNote. Cette énumération est nouvelle dans OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**heNone** <br/> |0  <br/> |Fait référence à aucun élément.  <br/> |
|**heNotebooks** <br/> |1  <br/> |Fait référence aux éléments bloc-notes.  <br/> |
|**heSectionGroups** <br/> |2  <br/> |Fait référence aux éléments de la Section groupe.  <br/> |
|**heSections** <br/> |4  <br/> |Fait référence aux éléments de la Section.  <br/> |
|**hePages** <br/> |8  <br/> |Fait référence aux éléments de Page.  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

Lorsqu’il est passé à la méthode **GetHierarchy** , spécifie le niveau le plus bas à obtenir dans la hiérarchie de nœud bloc-notes. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |0  <br/> |Obtient uniquement le nœud de départ spécifié et aucun descendant.  <br/> |
|**hsChildren** <br/> |1  <br/> |Obtient l’enfant immédiat nœuds du nœud de départ et aucun descendant dans des groupes de sous-section supérieures ou inférieures.  <br/> |
|**hsNotebooks** <br/> |2  <br/> |Obtient tous les ordinateurs portables sous le nœud de départ, ou racine.  <br/> |
|**hsSections** <br/> |3  <br/> |Obtient toutes les sections en dessous du nœud de démarrage, y compris les sections dans la section et les groupes de sous-section.  <br/> |
|**hsPages** <br/> |4  <br/> |Obtient toutes les pages en dessous du nœud de démarrage, y compris toutes les pages dans la section et les groupes de sous-section.  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

Lorsqu’il est passé à la méthode **CreateNewPage** , spécifie le style de la nouvelle page. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |0  <br/> |Crée une page qui contient le style de page par défaut.  <br/> |
|**npsBlankPageWithTitle** <br/> |1  <br/> |Crée une page vierge qui possède un titre.  <br/> |
|**npsBlankPageNoTitle** <br/> |2  <br/> |Crée une page vierge sans titre.  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

Lorsqu’il est passé à la méthode **NotebookFilterOut** de l’objet **QFD** , spécifie les blocs-notes à afficher lorsque la zone QFD s’affiche. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1  <br/> |Autoriser uniquement les ordinateurs portables Local.  <br/> |
|**nfoNetwork** <br/> |2  <br/> |Permet à SharePoint blocs-notes ou UNC.  <br/> |
|**nfoWeb** <br/> |4  <br/> |Permet de blocs-notes OneDrive.  <br/> |
|**nfoNoWacUrl** <br/> |8  <br/> |Les ordinateurs portables dans les emplacements qui n’ont pas d’un client web.  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (mis à jour pour OneNote 2013)
<a name="odc_PageInfo"> </a>

Lorsqu’il est passé à la méthode **GetPageContent** , spécifie le type d’informations à renvoyer avec le contenu de page. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**piBasic** <br/> |0  <br/> |Renvoie le contenu de page de base uniquement, sans le balisage de la sélection, types de fichiers pour les objets de données binaires et les données binaires. Il s’agit de la valeur standard à passer.  <br/> |
|**piBinaryData** <br/> |1  <br/> |Renvoie la page contenu aucune balise de sélection, mais avec toutes les données binaires.  <br/> |
|**piSelection** <br/> |2  <br/> |Renvoie la page contenu avec le balisage de la sélection, mais pas de données binaires.  <br/> |
|**piBinaryDataSelection** <br/> |3  <br/> |Renvoie la page de contenu avec le balisage de sélection et de toutes les données binaires.  <br/> |
|**piFileType** <br/> |4  <br/> |Renvoie la page de contenu avec les informations de type de fichier pour les objets de données binaires.  <br/> |
|**piBinaryDataFileType** <br/> |5  <br/> |Renvoie la page de contenu avec les informations de type de fichier pour les objets de données binaires et les données binaires  <br/> |
|**piSelectionFileType** <br/> |6  <br/> |Renvoie la page de contenu avec le balisage et le fichier type Infos sur la sélection pour les données binaires.  <br/> |
|**piAll** <br/> |7  <br/> |Renvoie le contenu de la page.  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Lorsqu’il est passé à la méthode de **publication** , spécifie le format dans lequel s’affiche la page publiée. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |0  <br/> |Page publiée est au format .one.  <br/> |
|**pfOneNotePackage** <br/> |1  <br/> |Page publiée est au format .onepkg.  <br/> |
|**pfMHTML** <br/> |2  <br/> |Page publiée est au format .mht.  <br/> |
|**pfPDF** <br/> |3  <br/> |Page publiée est au format .pdf.  <br/> |
|**pfXPS** <br/> |4  <br/> |Page publiée est au format .xps.  <br/> |
|**pfWord** <br/> |5  <br/> |Page publiée est au format .doc ou .docx.  <br/> |
|**pfEMF** <br/> |6  <br/> |Page publiée est au format de métafichier amélioré (.emf).  <br/> |
|**pfHTML** <br/> |7  <br/> |Page publiée est au format .html. Ce membre est nouveau dans OneNote 2013.  <br/> |
|**pfOneNote2007** <br/> |8  <br/> |Page publiée est au format .one 2007. Ce membre est nouveau dans OneNote 2013.  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

Lorsqu’il est passé à la méthode **SetRecentResults** de l’objet **IQuickFilingDialog** , spécifie quelle liste résultats récents à afficher lorsque la boîte de dialogue classement rapide s’affiche. Listes de résultats récents sont utilisés pour effectuer le suivi de l’ensemble des emplacements de OneNote que l’utilisateur sélectionne dans la boîte de dialogue classement rapide. Il existe trois listes de résultat récent dans OneNote 2013 qui effectuent le suivi de classement, recherche et la liaison des actions. Cette énumération est nouvelle dans OneNote 2013. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |0  <br/> |Ne définit aucune liste de résultat récent à afficher.  <br/> |
|**rrtFiling** <br/> |1  <br/> |Définit la liste récente « Classement » pour être affiché.  <br/> |
|**rrtSearch** <br/> |2  <br/> |Définit la liste de résultat récent « Search » pour être affiché.  <br/> |
|**rrtLinks** <br/> |3  <br/> |Définit la liste de résultat récent « Liens » pour être affiché.  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

Lorsqu’il est passé à la méthode **GetSpecialLocation** , spécifie le chemin d’accès de l’emplacement spécial à obtenir. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |0  <br/> |Obtient le chemin d’accès à l’emplacement du dossier des dossiers de sauvegarde.  <br/> |
|**slUnfiledNotesSection** <br/> |1  <br/> |Obtient le chemin d’accès à l’emplacement du dossier Notes non classées.  <br/> |
|**slDefaultNotebookFolder** <br/> |2  <br/> |Obtient le chemin d’accès à l’emplacement du dossier par défaut le bloc-notes.  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

Lorsqu’il est passé à la méthode **TreeCollapsedState** de l’objet **QFD** , spécifie si l’arborescence de la hiérarchie doit être développé ou réduit. 
  
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |0  <br/> |Définit l’arborescence développée.  <br/> |
|**tcsCollapsed** <br/> |1  <br/> |Définit l’arborescence hiérarchique réduite.  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (mis à jour pour OneNote 2013)
<a name="odc_SpecialLocation"> </a>

Lorsqu’il est passé à une des méthodes suivantes, spécifie la version du schéma XML de OneNote à utiliser :
  
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.FindMeta**
    
- **OneNote15.Application.FindPages**
    
- **OneNote15.Application.GetHierarchy**
    
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.UpdateHierarchy**
    
- **OneNote15.Application.UpdatePageContent**
    
|**Membre**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**xs2007** <br/> |0  <br/> |Référence du schéma de OneNote 2007.  <br/> |
|**xs2010** <br/> |1  <br/> |Référence du schéma de OneNote 2010.  <br/> |
|**xs2013** <br/> |2  <br/> |Référence du schéma de OneNote 2013.  <br/> |
|**xsCurrent** <br/> |2  <br/> |Référence du schéma de la version actuelle de OneNote.  <br/> <br/>**Remarque**: nous ne recommandons pas l’utilisation de **xsCurrent** dans la plupart des cas, comme il peut entraîner des problèmes de compatibilité avec les futures versions de OneNote. Au lieu de cela spécifier la version du schéma que votre application a été conçue pour gérer, comme xs2013.           |
   
## <a name="see-also"></a>Voir aussi

- [Référence du développeur OneNote](onenote-developer-reference.md)


---
title: Rapides interfaces boîte de dialogue remplissage (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: Cette rubrique décrit les interfaces que vous pouvez utiliser pour personnaliser par programme la boîte de dialogue classement rapide dans OneNote 2013.
ms.openlocfilehash: c820765f1a4a19c4576ac8e6ed0bbf6cc140f1dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572262"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Rapides interfaces boîte de dialogue remplissage (OneNote 2013)

Cette rubrique décrit les interfaces que vous pouvez utiliser pour personnaliser par programme la boîte de dialogue classement rapide dans OneNote 2013.
  
## <a name="quick-filing-dialog-box"></a>Boîte de dialogue Classement rapide

La boîte de dialogue classement rapide dans OneNote 2013 est une boîte de dialogue personnalisable qui permet aux utilisateurs de sélectionner un emplacement au sein de la structure de la hiérarchie OneNote. Emplacements sélectionnables incluent les ordinateurs portables, les groupes de sections, sections, pages et des sous-pages. La boîte de dialogue est utilisée au sein de l'application OneNote et par des applications externes par le biais de l'API OneNote 2013. La figure 1 montre la boîte de dialogue classement rapide dans son état par défaut.
  
**La figure 1. Boîte de dialogue Remplissage rapide sans personnalisations**

![Boîte de dialogue Remplissage rapide sans personnalisations](media/ON15Con_quick_filing_dialog.jpg "Boîte de dialogue Remplissage rapide sans personnalisations")
  
Dans la boîte de dialogue, les utilisateurs peuvent parcourir la hiérarchie de tous les ordinateurs portables pour rechercher les emplacements spécifiques ou rechercher dans la structure d'arborescence OneNote en tapant dans la zone de texte. Aspects de la boîte de dialogue qui peuvent être personnalisés incluent le titre, description, récente liste des résultats, texte de la case à cocher État, profondeur de l'arborescence, boutons et des types d'emplacements sélectionnable.

Vous pouvez accéder à la fonctionnalité de boîte de dialogue classement rapide via deux interfaces OneNote 2013. L'interface **IQuickFilingDialog** permet aux utilisateurs d'instancier, configurer et exécuter la boîte de dialogue. L'interface **IQuickFilingDialogCallback** est appelé après la fermeture de la boîte de dialogue. La boîte de dialogue est exécutée dans le processus de OneNote, un mécanisme n'est nécessaire pour conserver un thread de la boîte de dialogue en cours d'exécution, puis pour capturer la sélection de l'utilisateur et l'état de la boîte de dialogue lors de sa fermeture. 
  
## <a name="iquickfilingdialog-interface"></a>Interface IQuickFilingDialog
<a name="odc_IQuickFilingDialog"> </a>

Cette interface autorise l'utilisateur à personnaliser et exécuter la boîte de dialogue. L'utilisateur peut instancier une boîte de dialogue par le biais de la classe **Application** à l'aide de la méthode **Application.QuickFilingDialog**. La méthode retourne une instance de la boîte de dialogue. Une fois que les propriétés de la boîte de dialogue sont définies, la méthode **IQuickFilingDialog.Run** est utilisée pour exécuter la boîte de dialogue. Cette méthode exécute la boîte de dialogue sur un nouveau thread. 
  
**Propriétés**

|**Name**|**Type**|**Description**|
|:-----|:-----|:-----|
|**Title** <br/> |string  <br/> |Obtient ou définit le texte du titre qui s'affiche dans la barre de titre de la fenêtre de boîte de dialogue.  <br/> |
|**Description** <br/> |string  <br/> |Obtient ou définit la description de texte pour indiquer à l'utilisateur sur les éléments à sélectionner. Cette valeur peut être texte multiligne.  <br/> |
|**CheckboxText** <br/> |string  <br/> |Obtient ou définit le texte qui suit la case à cocher. Si cette valeur est définie sur une chaîne non vide, une case à cocher apparaît dans la boîte de dialogue. Si la valeur est une chaîne vide, aucune case à cocher s'affiche.  <br/> |
|**CheckboxState** <br/> |bool  <br/> |Obtient ou définit l'état de la case à cocher. Si la valeur est définie sur **false**, la case à cocher est désactivée au démarrage de la boîte de dialogue. Si la valeur est définie sur **true**, la case à cocher est activée lorsque la boîte de dialogue est démarrée en tant que **CheckboxText** est une chaîne vide.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Obtient l'ID de handle de la fenêtre de boîte de dialogue classement rapide.  <br/> |
|**TreeDepth** <br/> |**HierarchyElement** <br/> |Obtient ou définit la profondeur l'arborescence OneNote doit être affiché dans la section tous les ordinateurs portables. Par défaut, l'arborescence est affichée aux sections. Cette propriété n'affecte pas le type d'éléments peut être sélectionné. <br/> Si **TreeDepth** est défini sur un élément plus bas dans la hiérarchie OneNote que peuvent être sélectionnés par un des boutons, la profondeur de l'arborescence affichée sera l'élément sélectionnable possible la plus faible. En d'autres termes, si la profondeur de l'arborescence est définie à afficher aux pages, mais l'élément sélectionnable le plus bas est une section, l'arborescence est affichée aux sections.  <br/> |
|**ParentWindowHandle** <br/> |ulong  <br/> |Obtient ou définit l'ID du handle de la fenêtre parente de la boîte de dialogue. Si cette propriété est définie, la boîte de dialogue classement rapide sera modale par rapport à la fenêtre parent affecté lorsque la boîte de dialogue s'ouvre. En d'autres termes, un utilisateur ne sera pas en mesure d'accéder à la fenêtre parent jusqu'à la fermeture de la boîte de dialogue classement rapide.  <br/> |
|**Position** <br/> |tagPOINT  <br/> |Obtient ou définit la position de la fenêtre par rapport à l'écran. Par défaut, la boîte de dialogue s'affiche au milieu de la fenêtre parent ou le bureau.  <br/> |
|**SelectedItem** <br/> |string  <br/> |Obtient l'ID d'objet de l'emplacement de OneNote sélectionnée par l'utilisateur lors de la fermeture de la boîte de dialogue. Si l'utilisateur clique sur le bouton **Annuler**, l'objet est définie sur null. <br/> |
|**PressedButton** <br/> |ulong  <br/> |Obtient quel bouton a été utilisé lors de la fermeture de la boîte de dialogue. Si l'utilisateur a cliqué sur le bouton **Annuler**, cette propriété renvoie la valeur -1. Tous les autres boutons sont affectées des valeurs entières à partir de 0, est incrémentée de 1 pour chaque bouton ajouté à la boîte de dialogue. La valeur entière du bouton **OK** par défaut est 0.  <br/> |
   
### <a name="methods"></a>Méthodes

**SetRecentResults**

|||
|:-----|:-----|
|**Description** <br/> |Définit quelle liste résultats récents s'affichera dans la boîte de dialogue classement rapide et indique s'il faut inclure certains emplacements spéciaux classement dans la liste. Les utilisateurs peuvent sélectionner une liste de résultats récents à partir de l'énumération [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) . Les utilisateurs peuvent également choisir d'ajouter les options suivantes à la liste : Section en cours, Page en cours ou Notes non classées. Si **RecentResultType.rrtNone** est sélectionné, aucune liste de résultats récents n'est indiqué.  <br/> |
|**Syntaxe** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Paramètres** <br/> | _recentResults_ &ndash; Objet de type **RecentResultType** qui indique la liste des résultats récents, le cas caser, qui doit apparaître. Si **rrtNone** est sélectionné, aucune liste de résultats récents n'apparaît dans la boîte de dialogue.<br/><br/>  _fShowCurrentSection_ &ndash; Valeur Boolean qui indique si la section actuelle doit être incluse dans la liste des résultats récents.<br/><br/>  _fShowCurrentPage_ &ndash; Valeur Boolean qui indique si la page actuelle doit être incluse dans la liste des résultats récents.<br/><br/>  _fShowUnfiledNotes_ &ndash; Valeur Boolean qui indique si la section Notes non filtrées doit être incluse dans la liste des résultats récents.  <br/> |
   
> [!NOTE]
> [!REMARQUE] Si un emplacement de la classification spéciaux ne peuvent pas être sélectionné à l'aide d'un des boutons dans la boîte de dialogue, il n'est pas affiché dans la liste. Si aucun élément sélectionnable dans la liste des résultats récents n'est trouvée, aucune liste de résultats récents ne s'affiche. 
  
L'exemple suivant utilise la méthode **SetRecentResults** pour afficher la section en cours, page en cours et la section Notes non classées dans la liste de résultats récents. 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

**AddButton**

|||
|:-----|:-----|
|**Description** <br/> |Permet aux utilisateurs d'ajouter et personnaliser des boutons dans la boîte de dialogue. Les utilisateurs peuvent spécifier le texte sur les boutons et les éléments de la hiérarchie de OneNote peuvent être sélectionnés par chaque bouton.  <br/> |
|**Syntaxe** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Paramètres** <br/> | _bstrText_ &ndash; Chaîne qui spécifie le texte à apparaître sur le bouton. Pour personnaliser le bouton **OK** par défaut, passez une valeur null en tant que **bstrText**.  <br/><br/>_allowedElements_ &ndash; Élément **HierarchyElement** qui indique les éléments de hiérarchie en lecture OneNote qu’un utilisateur est autorisé à sélectionner à l’aide du bouton. Pour sélectionner plusieurs éléments, l'utilisateur doit passer l'opérateur **OR** pour toutes les valeurs d'équivalente uint des types **HierarchyElement** autorisés comme un **HierarchyElement**.<br/><br/>  _allowedReadOnlyElements_ &ndash; Élément **HierarchyElement** qui indique les éléments OneNote hiérarchie en lecture seule qu’un utilisateur est autorisé à sélectionner à l’aide du bouton. Pour sélectionner plusieurs éléments, l'utilisateur doit passer l'opérateur **OR** pour toutes les valeurs d'équivalents **uint** des types **HierarchyElement** autorisés comme un **HierarchyElement**.<br/><br/>  _fDefault_ &ndash; Valeur boolé américaine qui spécifie si ce bouton doit être le bouton par défaut. Si plusieurs boutons sont définis en tant que valeur par défaut, le bouton dernier spécifié devienne le bouton par défaut.  <br/> |
   
L'exemple suivant ajoute trois boutons à la boîte de dialogue classement rapide. La première condition, **ensemble**, peut être sélectionnée par tous les éléments dans l'arborescence de la hiérarchie OneNote. Les autres, **les ordinateurs portables** et les **Pages**, peuvent être sélectionnés uniquement si leurs éléments correspondants, les ordinateurs portables et les Pages, sont sélectionnés.
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

**Run**

|||
|:-----|:-----|
|**Description** <br/> |Affiche la boîte de dialogue classement rapide à partir d'un thread. Elle accepte une référence à l'interface **IQuickFilingDialogCallback**, dont la méthode **OnDialogClosed** sera appelée une fois que la boîte de dialogue se ferme.  <br/> |
|**Syntaxe** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Paramètres** <br/> | _piCallback_ &ndash; Référence à l’interface **IQuickFilingDialogCallback** qui sera ins instantiée une fois la boîte de dialogue refermée.  <br/> |
   
L'exemple suivant utilise la méthode **Run** pour afficher la boîte de dialogue classement rapide à partir d'un thread. 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

**TreeCollapsedState**

|||
|:-----|:-----|
|**Description** <br/> |Indique si l'arborescence de la hiérarchie doit être développé ou réduit.  <br/> |
|**Syntaxe** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Paramètres** <br/> | _tcs_ - Spécifie si l'arborescence est développée ou réduite.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Description** <br/> |Filtre la liste des ordinateurs portables indiqué par type.  <br/> |
|**Syntaxe** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Paramètres** <br/> | _nfo_ - Spécifie l'ensemble des ordinateurs portables qui doivent être filtrées en dehors de la liste  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Description** <br/> |Affiche l'option créer un nouveau bloc-notes dans la boîte de dialogue.  <br/> |
|**Syntaxe** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Paramètres** <br/> |Aucune  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Description** <br/> |Ajoute un utilisateur comme un éditeur initial dans un bloc-notes dans la boîte de dialogue classement rapide.  <br/> |
|**Syntaxe** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Paramètres** <br/> | _initialEditor_ - adresse de messagerie de l'utilisateur que vous souhaitez ajouter en tant qu'éditeur dans le bloc-notes. Lorsque l'ordinateur portable est créé par le biais de la boîte de dialogue classement rapide, il est automatiquement partagé avec tous les éditeurs initiale.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Description** <br/> |Supprime tous les éditeurs initiales de la boîte de dialogue classement rapide.  <br/> |
|**Syntaxe** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Paramètres** <br/> |Aucun  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Description** <br/> |Afficher le lien hypertexte dans l'aide de partage dans la boîte de dialogue classement rapide.  <br/> |
|**Syntaxe** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Paramètres** <br/> |Aucun  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>Interface IQuickFilingDialogCallback
<a name="odc_IQuickFilingDialog"> </a>

Cette interface autorise l'utilisateur à accéder à la boîte de dialogue Propriétés après la fermeture de la boîte de dialogue. Une fois que la boîte de dialogue se ferme, OneNote 2013 appelle la méthode **IQuickFilingDialogCallback.OnDialogClose** dans cette interface. 
  
Une classe qui hérite de cette interface doit être défini.
  
### <a name="methods"></a>Méthodes

La section suivante décrit les méthodes associées aux interfaces détaillées précédemment.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Description** <br/> |Permet aux utilisateurs d'ajouter des fonctionnalités permettant de capturer et utiliser la sélection de l'utilisateur à partir de la boîte de dialogue. Cette méthode est appelée après la fermeture de la boîte de dialogue classement rapide. Cette méthode est une fonction dont les interfaces **IQuickFilingDialogCallback** à définir.  <br/> |
|**Syntaxe** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Paramètres** <br/> | _boîte de dialogue_ &ndash; Objet **IQuickFilingDialog** qui a appelé **la méthode OnDialogClose.**  <br/> |
   
L'exemple suivant est un exemple d'interface **IQuickFilingDialogCallback**. La méthode **OnDialogClose** imprime la sélection de l'utilisateur à partir de la boîte de dialogue classement rapide sur la console. 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a>Exemple
<a name="odc_IQuickFilingDialog"> </a>

L'exemple de code suivant ouvre une boîte de dialogue classement rapide qui a un titre personnalisé, description, liste des derniers résultats, profondeur de l'arborescence, case à cocher et les boutons. L'utilisateur de l'élément, vous appuyez sur le bouton sélectionné et état de la case à cocher s'affiche dans une fenêtre de console lorsque la boîte de dialogue est fermée. Pour afficher le bouton de page activé, l'utilisateur aura rechercher une page et sélectionnez-le, car la profondeur de l'arborescence est fixée aux sections. La boîte de dialogue n'est pas un enfant de n'importe quelle fenêtre.
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a>Voir aussi

- [Référence du développeur OneNote](onenote-developer-reference.md)


---
title: QuitAccess, action de macro
TOCTitle: QuitAccess macro action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 793e6c2e57f50b5086780d8632952c45f3d4442d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997982"
---
# <a name="quitaccess-macro-action"></a><span data-ttu-id="f0788-102">QuitAccess, action de macro</span><span class="sxs-lookup"><span data-stu-id="f0788-102">QuitAccess macro action</span></span>

<span data-ttu-id="f0788-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0788-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0788-p101">Vous pouvez utiliser l'action **QuitterAccess** pour quitter Microsoft Access. L'action **QuitterAccess** peut également spécifier une des options d'enregistrement d'objets de base de données avant de quitter Access.</span><span class="sxs-lookup"><span data-stu-id="f0788-p101">You can use the **QuitAccess** action to exit Microsoft Access. The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.</span></span>

> [!NOTE]
> <span data-ttu-id="f0788-106">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="f0788-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="f0788-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f0788-107">Setting</span></span>

<span data-ttu-id="f0788-108">L'action **QuitterAccess** utilise l'argument suivant :</span><span class="sxs-lookup"><span data-stu-id="f0788-108">The **QuitAccess** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0788-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="f0788-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f0788-110">Description</span><span class="sxs-lookup"><span data-stu-id="f0788-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0788-111"><strong>Options</strong></span><span class="sxs-lookup"><span data-stu-id="f0788-111"><strong>Options</strong></span></span></p></td>
<td><p><span data-ttu-id="f0788-p102">Spécifie l’action appliquée aux objets non enregistrés lorsque vous quittez Access. Cliquez sur <strong>Avec confirmation</strong> (pour afficher des boîtes de dialogue qui vous demandent si vous souhaitez enregistrer chaque objet), sur <strong>Enregistrer tout</strong> (pour enregistrer tous les objets sans demander de confirmation) ou sur <strong>Quitter</strong> (pour quitter sans enregistrer d’objet) dans la zone <strong>Options</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. La valeur par défaut est <strong>Enregistrer tout</strong>.</span><span class="sxs-lookup"><span data-stu-id="f0788-p102">Specifies what happens to unsaved objects when you quit Access. Click <strong>Prompt</strong> (to display dialog boxes that ask whether to save each object), <strong>Save All</strong> (to save all objects without prompting by dialog boxes), or <strong>Exit</strong> (to quit without saving any objects) in the <strong>Options</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Save All</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f0788-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f0788-115">Remarks</span></span>

<span data-ttu-id="f0788-116">Access n'exécute aucune action après l'action **QuitterAccess** dans une macro.</span><span class="sxs-lookup"><span data-stu-id="f0788-116">Access doesn't run any actions that follow the **QuitAccess** action in a macro.</span></span>

<span data-ttu-id="f0788-p103">Cette action vous permet de quitter Access sans afficher de demande de confirmation dans les boîtes de dialogue **Enregistrer** en utilisant une commande de menu personnalisée ou un bouton dans un formulaire. Vous pouvez, par exemple, avoir un formulaire de base que vous utilisez pour afficher des objets dans votre espace de travail personnalisé. Ce formulaire peut comporter un bouton **Quitter** qui exécute une macro contenant l'action **QuitterAccess** avec la valeur **Enregistrer tout** définie pour l'argument **Options**.</span><span class="sxs-lookup"><span data-stu-id="f0788-p103">You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form. For example, you might have a master form that you use to display the objects in your custom workspace. This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.</span></span>

<span data-ttu-id="f0788-p104">Cette action équivaut à cliquer sur l'onglet **Fichier**, puis sur **Quitter**. Si des objets ne sont pas encore enregistrés lorsque vous cliquez sur cette commande, les boîtes de dialogue qui s'affichent sont identiques à celles qui apparaissent lorsque vous sélectionnez la valeur **Demander** pour l'argument **Options** de l'action **QuitterAccess**.</span><span class="sxs-lookup"><span data-stu-id="f0788-p104">This action has the same effect as clicking the **File** tab and then clicking **Exit**. If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.</span></span>

<span data-ttu-id="f0788-122">Vous pouvez utiliser l'action **EnregistrerObjet** d'une macro pour enregistrer un objet spécifié sans devoir quitter Access ou fermer l'objet.</span><span class="sxs-lookup"><span data-stu-id="f0788-122">You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.</span></span>

<span data-ttu-id="f0788-123">Pour exécuter l'action **QuitterAccess** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Quit** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="f0788-123">To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.</span></span>


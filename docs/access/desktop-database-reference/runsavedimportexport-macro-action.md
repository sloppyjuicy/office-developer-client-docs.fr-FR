---
title: ExécuterImportationExportationSauvegardée, action de macro
TOCTitle: RunSavedImportExport Macro Action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0afff780714f8be943a2b0b7d744d6118fcacf88
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471414"
---
# <a name="runsavedimportexport-macro-action"></a><span data-ttu-id="bd5b1-102">ExécuterImportationExportationSauvegardée, action de macro</span><span class="sxs-lookup"><span data-stu-id="bd5b1-102">RunSavedImportExport Macro Action</span></span>


<span data-ttu-id="bd5b1-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd5b1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bd5b1-104">L'action **ExécuterImportationExportationSauvegardée** vous permet d'exécuter une spécification d'importation ou d'exportation sauvegardée que vous avez créée à l'aide de l'Assistant Importation ou de l'Assistant Exportation.</span><span class="sxs-lookup"><span data-stu-id="bd5b1-104">You can use the **RunSavedImportExport** action to run a saved import or export specification that you created by using the Import Wizard or the Export Wizard.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bd5b1-p101">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="bd5b1-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="bd5b1-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd5b1-107">Setting</span></span>

<span data-ttu-id="bd5b1-108">L'action **ExécuterImportationExportationSauvegardée** possède l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="bd5b1-108">The **RunSavedImportExport** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd5b1-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="bd5b1-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="bd5b1-110">Description</span><span class="sxs-lookup"><span data-stu-id="bd5b1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd5b1-111"><strong>Nom de l'importation/exportation enregistrée</strong></span><span class="sxs-lookup"><span data-stu-id="bd5b1-111"><strong>Saved Import Export Name</strong></span></span></p></td>
<td><p><span data-ttu-id="bd5b1-112">Sélectionnez le nom d'une spécification d'importation ou d'exportation enregistrée dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="bd5b1-112">Select the name of a saved import or export specification from the drop-down list.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bd5b1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bd5b1-113">Remarks</span></span>

  - <span data-ttu-id="bd5b1-114">Cette action de macro équivaut à effectuer la procédure suivante dans Access :</span><span class="sxs-lookup"><span data-stu-id="bd5b1-114">This macro action has the same effect as performing the following procedure in Access:</span></span>
    
    1.  <span data-ttu-id="bd5b1-115">Sous l'onglet **Données externes**, cliquez sur **Importations enregistrées** ou sur **Exportations enregistrées**.</span><span class="sxs-lookup"><span data-stu-id="bd5b1-115">On the **External Data** tab, click either **Saved Imports** or **Saved Exports**.</span></span>
    
    2.  <span data-ttu-id="bd5b1-116">Dans la boîte de dialogue **Gérer les tâches de données**, sous l'onglet **Importations enregistrées** ou **Exportations enregistrées** (en fonction de votre choix à l'étape précédente), cliquez sur la spécification que vous voulez exécuter.</span><span class="sxs-lookup"><span data-stu-id="bd5b1-116">In the **Manage Data Tasks** dialog box, on the **Saved Imports** or **Saved Exports** tab (depending on your choice in the preceding step), click the specification that you want to run.</span></span>
    
    3.  <span data-ttu-id="bd5b1-117">Cliquez sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="bd5b1-117">Click **Run**.</span></span>

  - <span data-ttu-id="bd5b1-118">Avant d'exécuter l'action **ExécuterImportationExportationSauvegardée**, assurez-vous que les fichiers source et de destination existent, que les données sources sont prêtes à être importées et que l'opération ne risque pas de remplacer des données dans le fichier de destination.</span><span class="sxs-lookup"><span data-stu-id="bd5b1-118">Before running the **RunSavedImportExport** action, make sure that the source and destination files exist, the source data is ready for importing, and that the operation will not accidentally overwrite any data in your destination file.</span></span>

  - <span data-ttu-id="bd5b1-119">Des liens vers davantage d'informations sur l'enregistrement et l'exécution de spécifications d'importation et d'exportation sont disponibles à la section **Voir aussi**.</span><span class="sxs-lookup"><span data-stu-id="bd5b1-119">Find links to more information about saving and running import and export specifications in the **See Also** section.</span></span>

  - <span data-ttu-id="bd5b1-120">Si l’importation ou d’exportation enregistrée spécification choisie pour l’argument **Saved Import Export Name** est supprimée après la création de la macro, Access affiche le message d’erreur suivant lors de l’exécution de la macro : \*\*la spécification de l’index spécifié est existe pas. Spécifiez un autre index. ' \*\*\* spécification nom \***'.**</span><span class="sxs-lookup"><span data-stu-id="bd5b1-120">If the saved import or export specification you choose for the **Saved Import Export Name** argument is deleted after the macro is created, Access displays the following error message when the macro is run: **The specification with the specified index does not exist. Specify a different index. '\*\*\*\*\*specification name\*\*\*\*\*'.**</span></span>


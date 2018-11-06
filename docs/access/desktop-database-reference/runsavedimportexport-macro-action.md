---
title: RunSavedImportExport, action de macro
TOCTitle: RunSavedImportExport macro action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7f98076c147a55561adf2baf24b55274bbea463d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998846"
---
# <a name="runsavedimportexport-macro-action"></a>RunSavedImportExport, action de macro

**S’applique à**: Access 2013, Office 2013

L'action **ExécuterImportationExportationSauvegardée** vous permet d'exécuter une spécification d'importation ou d'exportation sauvegardée que vous avez créée à l'aide de l'Assistant Importation ou de l'Assistant Exportation.

> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.

## <a name="setting"></a>Valeur

L'action **ExécuterImportationExportationSauvegardée** possède l'argument suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nom de l'importation/exportation enregistrée</strong></p></td>
<td><p>Sélectionnez le nom d'une spécification d'importation ou d'exportation enregistrée dans la liste déroulante.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

- Cette action de macro équivaut à effectuer la procédure suivante dans Access :
    
  1.  Sous l'onglet **Données externes**, cliquez sur **Importations enregistrées** ou sur **Exportations enregistrées**.
    
  2.  Dans la boîte de dialogue **Gérer les tâches de données**, sous l'onglet **Importations enregistrées** ou **Exportations enregistrées** (en fonction de votre choix à l'étape précédente), cliquez sur la spécification que vous voulez exécuter.
    
  3.  Cliquez sur **Exécuter**.

- Avant d'exécuter l'action **ExécuterImportationExportationSauvegardée**, assurez-vous que les fichiers source et de destination existent, que les données sources sont prêtes à être importées et que l'opération ne risque pas de remplacer des données dans le fichier de destination.

- Des liens vers davantage d'informations sur l'enregistrement et l'exécution de spécifications d'importation et d'exportation sont disponibles à la section **Voir aussi**.

- Si l’importation ou d’exportation enregistrée spécification choisie pour l’argument **Saved Import Export Name** est supprimée après la création de la macro, Access affiche le message d’erreur suivant lors de l’exécution de la macro : **la spécification de l’index spécifié est existe pas. Spécifiez un autre index. ' *** spécification nom ***'.**


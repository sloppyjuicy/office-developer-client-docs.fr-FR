---
title: ImportSharePointList, action de macro
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726203"
---
# <a name="importsharepointlist-macro-action"></a>ImportSharePointList, action de macro

**S’applique à**: Access 2013, Office 2013

L'action **ImporterListeSharePoint** permet d'importer ou de lier des données à partir d'un site Microsoft SharePoint Foundation.

> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. 

## <a name="setting"></a>Valeur

L'action **ImporterListeSharePoint** utilise les arguments suivants :

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
<td><p><strong>Type de transfert</strong></p></td>
<td><p>Sélectionnez le type de transfert.</p>
<ul>
<li><p>Sélectionnez <strong>Importer</strong> pour copier les données Windows SharePoint Services dans une table Microsoft Access. Mises à jour les données dans Access n’affectent pas les données dans Windows SharePoint Services. De même, les mises à jour les données dans Windows SharePoint Services n’affectent pas les données dans Access.</p></li>
<li><p>Sélectionnez le <strong>lien</strong> pour créer une table attachée dans Access liée aux données dans Windows SharePoint Services. Mises à jour les données dans Access sont reflétées dans Windows SharePoint Services. De même, les mises à jour les données dans Windows SharePoint Services sont répercutées dans Access.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Adresse du site</strong></p></td>
<td><p>Entrez le chemin d’accès complet au site SharePoint.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ID de liste</strong></p></td>
<td><p>Entrez le nom ou GUID de la liste à transférer. Cet argument est obligatoire.</p></td>
</tr>
<tr class="even">
<td><p><strong>ID de vue</strong></p></td>
<td><p>Entrez le GUID de l’affichage de la liste que vous souhaitez utiliser. Omettez cet argument pour transférer toutes les lignes et colonnes de la liste.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nom de la table</strong></p></td>
<td><p>Entrez le nom à afficher pour la table ou la table attachée dans Access.</p></td>
</tr>
<tr class="even">
<td><p><strong>Valeurs d’affichage Liste de choix</strong></p></td>
<td><p>Cliquez sur <strong>Oui</strong> si les valeurs d’affichage des champs de recherche doivent être transférées à la place de l’identificateur utilisé pour effectuer la recherche.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

- L'exécution de cette action équivaut à cliquer sur **Liste SharePoint** dans le groupe **Importer** de l'onglet **Données externes**. Les arguments utilisés pour l'action correspondent à vos choix dans l'Assistant Données externes.

- Pour exécuter l'action **ImporterListeSharePoint** dans un module VBA, utilisez la méthode **TransferSharePointList** de l'objet **DoCmd**.

- Si vous spécifiez une liste ou un affichage qui n'existe pas, aucune erreur ne se produit, mais aucune donnée n'est transférée.

- Le GUID d'une liste ou d'un affichage est un identificateur unique hexadécimal qui identifie cette liste ou cet affichage. Le GUID doit respecter le format suivant, où chaque « F » est un nombre hexadécimal (de 0 à 9 ou de A à F).
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  Pour obtenir le GUID d'une liste ou d'un affichage à partir du site SharePoint, procédez comme suit :
    
  1. Ouvrez la liste dans SharePoint Foundation.
    
  2. Si l'affichage que vous recherchez n'est pas dans la liste, cliquez sur la flèche de la liste déroulante **Affichage** et sélectionnez l'affichage voulu.
    
  3. Cliquez sur la flèche de la liste déroulante **Affichage**, puis sélectionnez **Modifier cet affichage**.L'adresse dans la barre d'adresse du navigateur contient les GUID de la liste et de l'affichage. Le GUID de la liste est à la suite de **Liste=** et celui de l'affichage est à la suite de **Affichage=**. Cependant, dans l'adresse, chaque caractère **{** (accolade de gauche) est représenté par la chaîne **%7B**, chaque caractère **-** (tiret) est représenté par la chaîne **%2D** et chaque caractère **}** (accolade de droite) est représenté par la chaîne **%7D**. Par exemple:
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  Avant de pouvoir utiliser le GUID de l’adresse en tant qu’arguments dans cette action de macro, vous devez remplacer chaque chaîne **7 b %** avec le caractère **{** , remplacer chaque **% 2D** chaîne avec la **-** de caractères et remplacez chaque chaîne **% 7 D** avec le caractère **}** . N'incluez pas le caractère **&** (et commercial) qui suit la chaîne **%7D** dans le GUID de la liste.


---
title: Requery, action de macro
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 3ff41c7a1d22f58a8a462b82dcd080e442a7254e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611594"
---
# <a name="requery-macro-action"></a>Requery, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l'action **Actualiser** pour mettre à jour les données d'un contrôle spécifié de l'objet actif en actualisant la source du contrôle. Si aucun contrôle n'est spécifié, cette action actualise la source de l'objet lui-même. Utilisez cette action pour garantir que l'objet actif ou l'un de ses contrôles affiche les données les plus récentes.

## <a name="setting"></a>Paramètre

L’action **Actualiser** accepte l’argument suivant.

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
<td><p><strong>Nom du contrôle</strong></p></td>
<td><p>Nom du contrôle à mettre à jour. Entrez le nom du contrôle dans la zone <strong>Nom contrôle</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous devez utiliser uniquement le nom du contrôle, et non son identificateur complet, par exemple <strong>Formulaires</strong>!<em>nomformulaire</em>!<em>nomcontrôle</em>). Laissez cet argument vide pour actualiser la source de l’objet actif. Si l’objet actif est une feuille de données ou le jeu de résultats d’une requête, vous devez laisser cet argument vide.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L’action **Actualiser** effectue l’une des actions suivantes :

- Réexécute la requête sur laquelle est basé le contrôle ou l'objet.

- Affiche les enregistrements nouveaux ou modifiés et enlève les éventuels enregistrements supprimés de la table sur laquelle est basé le contrôle ou l'objet.

> [!NOTE]
> [!REMARQUE] L'action **Actualiser** n'affecte pas la position du pointeur d'enregistrement.

Les contrôles basés sur une requête ou une table comprennent :

- zones de liste et zones de liste modifiable ;

- contrôles de sous-formulaire ;

- des objets OLE, tels que des graphiques ;

- des contrôles contenant des fonctions de domaine, telles que **DSum**.

Si le contrôle spécifié n'est pas basé sur une requête ou une table, cette action force un recalcul du contrôle.

Si vous laissez l'argument **Nom du contrôle** vide, l'action **Actualiser** équivaut à appuyer sur Maj+F9 lorsque l'objet a le focus. Si un contrôle sous-formulaire a le focus, cette action actualise seulement la source du sous-formulaire (comme lorsque vous appuyez sur les touches Maj+F9).

> [!NOTE]
> [!REMARQUE] L'action **Actualiser** actualise la source du contrôle ou de l'objet. En revanche, l'action **Redessiner** redessine les contrôles dans l'objet spécifié mais n'actualise pas la base de données et n'affiche pas les nouveaux enregistrements. L'action **AfficherTousEnreg** actualise non seulement l'objet actif mais supprime également tous les filtres appliqués, ce que ne fait pas l'action **Actualiser**.

Pour actualiser un contrôle qui ne figure pas dans l'objet actif, vous devez utiliser la méthode **Requery** dans un module Visual Basic pour Applications (VBA), et non l'action **Actualiser** ou sa méthode **Requery** correspondante de l'objet **DoCmd**. La méthode **Requery** dans VBA est plus rapide que l'action **Actualiser** ou la méthode **DoCmd.Requery**. En outre, lorsque vous utilisez l'action **Actualiser** ou la méthode **DoCmd.Requery**, Microsoft Access ferme la requête et la recharge à partir de la base de données tandis qu'avec la méthode **Requery**, réexécute la requête sans la fermer ni la charger. Notez que la méthode ActiveX **Requery** de l’objet Data object (ADO) fonctionne de la même manière que la méthode **Requery** Access.


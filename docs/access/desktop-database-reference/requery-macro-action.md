---
title: Actualiser, action de macro
TOCTitle: Requery Macro Action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9eea9445912b1a784d9926b2c044c4385a17ee69
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471518"
---
# <a name="requery-macro-action"></a>Actualiser, action de macro


**S’applique à**: Access 2013 | Office 2013

Vous pouvez utiliser l'action **Actualiser** pour mettre à jour les données d'un contrôle spécifié de l'objet actif en actualisant la source du contrôle. Si aucun contrôle n'est spécifié, cette action actualise la source de l'objet lui-même. Utilisez cette action pour garantir que l'objet actif ou l'un de ses contrôles affiche les données les plus récentes.

## <a name="setting"></a>Valeur

L'action **Actualiser** accepte l'argument suivant.

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
<td><p><strong>Nom du contrôle</strong> :</p></td>
<td><p>Nom du contrôle à mettre à jour. Entrez le nom du contrôle dans la zone <strong>Nom contrôle</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous devez utiliser uniquement le nom du contrôle, et non son identificateur complet, par exemple <strong>Formulaires</strong>!<em>nomformulaire</em>!<em>nomcontrôle</em>). Laissez cet argument vide pour actualiser la source de l’objet actif. Si l’objet actif est une feuille de données ou le jeu de résultats d’une requête, vous devez laisser cet argument vide.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

L'action **Actualiser** effectue l'une des actions suivantes :

  - Réexécute la requête sur laquelle est basé le contrôle ou l'objet.

  - Affiche les enregistrements nouveaux ou modifiés et enlève les éventuels enregistrements supprimés de la table sur laquelle est basé le contrôle ou l'objet.


> [!NOTE]
> <P>[!REMARQUE] L'action <STRONG>Actualiser</STRONG> n'affecte pas la position du pointeur d'enregistrement.</P>



Les contrôles basés sur une requête ou une table comprennent :

  - des zones de liste et des zones de liste déroulante ;

  - des contrôles sous-formulaires ;

  - des objets OLE, tels que des graphiques ;

  - des contrôles contenant des fonctions de domaine, telles que **DSum**.

Si le contrôle spécifié n'est pas basé sur une requête ou une table, cette action force un recalcul du contrôle.

Si vous laissez l'argument **Nom du contrôle** vide, l'action **Actualiser** équivaut à appuyer sur Maj+F9 lorsque l'objet a le focus. Si un contrôle sous-formulaire a le focus, cette action actualise seulement la source du sous-formulaire (comme lorsque vous appuyez sur les touches Maj+F9).


> [!NOTE]
> <P>[!REMARQUE] L'action <STRONG>Actualiser</STRONG> actualise la source du contrôle ou de l'objet. En revanche, l'action <STRONG>Redessiner</STRONG> redessine les contrôles dans l'objet spécifié mais n'actualise pas la base de données et n'affiche pas les nouveaux enregistrements. L'action <STRONG>AfficherTousEnreg</STRONG> actualise non seulement l'objet actif mais supprime également tous les filtres appliqués, ce que ne fait pas l'action <STRONG>Actualiser</STRONG>.</P>



Pour actualiser un contrôle qui ne figure pas dans l'objet actif, vous devez utiliser la méthode **Requery** dans un module Visual Basic pour Applications (VBA), et non l'action **Actualiser** ou sa méthode **Requery** correspondante de l'objet **DoCmd**. La méthode **Requery** dans VBA est plus rapide que l'action **Actualiser** ou la méthode **DoCmd.Requery**. En outre, lorsque vous utilisez l'action **Actualiser** ou la méthode **DoCmd.Requery**, Microsoft Access ferme la requête et la recharge à partir de la base de données tandis qu'avec la méthode **Requery**, réexécute la requête sans la fermer ni la charger. Notez que la méthode **Requery** ADO (ActiveX Data Object) fonctionne de la même manière que la méthode **Requery** d'Access.


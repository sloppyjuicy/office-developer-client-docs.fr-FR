---
title: Recordset2.EOF, propriété (DAO)
TOCTitle: EOF Property
ms:assetid: 9d4e1ee2-e866-3ebf-e08b-b31b0cb47ed9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198245(v=office.15)
ms:contentKeyID: 48546622
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052886
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 95b5d306684c7fd305ac9ffd0ff6bbefd1f83bd1
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629789"
---
# <a name="recordset2eof-property-dao"></a>Recordset2.EOF, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur qui indique si la position d'enregistrement actuelle suit le dernier enregistrement d'un objet **Recordset**. **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* .EOF

*expression* Variable qui représente un **objet Recordset2** .

## <a name="remarks"></a>Remarques

Vous pouvez utiliser la **BOF** et **EOF** propriétés pour déterminer si un **jeu d’enregistrements** objet contient des enregistrements ou que vous avez dépassé au-delà des limites d’un **Jeu d’enregistrements** lorsque vous déplacez à partir d’un enregistrement à l’objet.

Détermine l’emplacement du pointeur d’enregistrement actuel le **BOF** et **EOF** retournent des valeurs.

Si deux le **BOF** ou **EOF** propriété est **vrai**, il n’est aucun enregistrement actif.

Si vous ouvrez un **jeu d’enregistrements** objet ne contenant aucun enregistrement, la **BOF** et **EOF** propriétés sont définies sur **vrai** et le **Jeu d’enregistrements** d’objet **RecordCount** paramètre de la propriété est égal à 0. Lorsque vous ouvrez un **jeu d’enregistrements** objet qui contient au moins un enregistrement, le premier enregistrement est l’enregistrement actif et le **BOF** et **EOF** propriétés sont **Faux**; ils restent **faux** jusqu'à ce que vous déplacez au-delà de début ou à la fin de la **jeu d’enregistrements** objet à l’aide de la **MovePrevious** ou **MoveNext** méthode, respectivement. Lorsque vous déplacez au-delà de début ou à la fin de la **jeu d’enregistrements**, il n’est aucun enregistrement actif ou n’existe aucun enregistrement.

Si vous supprimez le dernier enregistrement restant dans la **jeu d’enregistrements** objet, le **BOF** et **EOF** propriétés peuvent restent **faux** jusqu'à ce que vous tentative de repositionner l’enregistrement actif.

Si vous utilisez le **MoveLast** méthode sur un **jeu d’enregistrements** objet contenant les enregistrements, le dernier enregistrement devient l’enregistrement actif ; si vous utilisez ensuite la **MoveNext** méthode, la version actuelle enregistrement devient non valide et le **EOF** propriété est définie sur **vrai**. À l’inverse, si vous utilisez le **MoveFirst** méthode sur un **jeu d’enregistrements** objet contenant les enregistrements, le premier enregistrement devient l’enregistrement actif ; si vous utilisez ensuite la **MovePrevious** méthode, il n’est aucun enregistrement actif et le **BOF** propriété est définie sur **vrai**.

En règle générale, lorsque vous travaillez avec tous les enregistrements dans une **jeu d’enregistrements** objet, votre code sera parcourir les enregistrements à l’aide de la **MoveNext** méthode jusqu'à ce que le **EOF** propriété est définie pour **vrai**.

Si vous utilisez le **MoveNext** méthode lors de la **EOF** propriété est définie sur **vrai** ou le **MovePrevious** méthode lors de la **BOF** propriété est définie sur **vrai**, une erreur se produit.

Le tableau suivant répertorie les méthodes Move sont autorisés avec différentes combinaisons de la **BOF** et **EOF** propriétés.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Move &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Move &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF=True,</strong><br />
<strong>EOF=False</strong></p></td>
<td><p>Autorisé</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
<td><p>Autorisé</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF=False,</strong><br />
<strong>EOF=True</strong></p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
</tr>
<tr class="odd">
<td><p>Les deux <strong>vrai</strong></p></td>
<td><p>Error</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
<td><p>Error</p></td>
</tr>
<tr class="even">
<td><p>Les deux <strong>faux</strong></p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
</tr>
</tbody>
</table>


Autoriser une méthode de déplacement ne signifie pas que la méthode parviendra à localiser un enregistrement. Il indique simplement qu’une tentative d’effectuer la méthode de déplacement spécifiée est autorisée et ne génère une erreur. L’état de la **BOF** et **EOF** propriétés peuvent changer suite au déplacement a été lancée.

Un **OpenRecordset** méthode appelle en interne une **MoveFirst** méthode. Par conséquent, à l’aide un **OpenRecordset** méthode sur un ensemble de jeux d’enregistrements vide le **BOF** et **EOF** propriétés à **vrai**. (Reportez-vous au tableau suivant pour le comportement d’une situation d’échec **MoveFirst** méthode.)

Toutes les méthodes de déplacement qui correctement localiser un enregistrement configurera les deux **BOF** et **EOF** à **faux**.

Dans un espace de travail Microsoft Access, si vous ajoutez un enregistrement à un vide **jeu d’enregistrements**, **BOF** deviendra **faux**, mais **EOF** restent **True**, indiquant que la position actuelle est à la fin de **jeu d’enregistrements**.

N’importe quel **supprimer** méthode, même si elle supprime du seul enregistrement restant à partir d’un **jeu d’enregistrements**, ne modifiez le paramètre de la **BOF** ou **EOF** propriété.

Le tableau suivant montre comment déplacer des méthodes qui ne localiser un enregistrement affectent la **BOF** et **EOF** paramètres de propriété.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>BOF</p></th>
<th><p>EOF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>MoveFirst</strong>, <strong>MoveLast</strong></p></td>
<td><p><strong>True</strong></p></td>
<td><p><strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong></strong>Move</p></td>
<td><p>Aucune modification</p></td>
<td><p>Aucune modification</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</p></td>
<td><p><strong>True</strong></p></td>
<td><p>Aucune modification</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</p></td>
<td><p>Aucune modification</p></td>
<td><p><strong>True</strong></p></td>
</tr>
</tbody>
</table>


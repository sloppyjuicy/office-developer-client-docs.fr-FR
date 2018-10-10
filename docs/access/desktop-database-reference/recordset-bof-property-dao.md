---
title: Recordset.BOF Property (DAO)
TOCTitle: BOF Property
ms:assetid: c50a0c5f-1b26-33ea-4cf2-311f9514a94a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823092(v=office.15)
ms:contentKeyID: 48547603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b54e373a1350a052250206d84ad978b6b9dabd0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471078"
---
# <a name="recordsetbof-property-dao"></a>Recordset.BOF Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Renvoie une valeur qui indique si la position de l'enregistrement actif est située avant le premier enregistrement dans un objet **Recordset**. Valeur de type **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . BOF

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Vous pouvez utiliser les propriétés **BOF** et **EOF** pour déterminer si un objet **Recordset** contient des enregistrements ou si vous avez dépassé les limites de l'objet **Recordset** en vous déplaçant d'un enregistrement à l'autre.

L'emplacement du pointeur d'enregistrement actif détermine les valeurs renvoyées par **BOF** et **EOF**.

Si la propriété **BOF** ou **EOF** a la valeur **True**, il n'existe aucun enregistrement actif.

Si vous ouvrez un objet **Recordset** qui ne contient aucun enregistrement, les propriétés **BOF** et **EOF** ont la valeur **True** et le paramètre de la propriété **RecordCount** de l'objet **Recordset** est égal à 0. Lorsque vous ouvrez un objet **Recordset** qui contient au moins un enregistrement, le premier enregistrement est l'enregistrement actif et les propriétés **BOF** et **EOF** ont la valeur **False**; elles conservent la valeur **False** jusqu'à ce que vous dépassiez la limite (début ou fin) de l'objet **Recordset** à l'aide des méthodes **MovePrevious** ou **MoveNext**. Lorsque vous dépassez le début ou la fin de l'objet **Recordset**, aucun enregistrement n'existe ou n'est actif.

Si vous supprimez le dernier enregistrement restant dans l'objet **Recordset**, les propriétés **BOF** et **EOF** conservent la valeur **False** jusqu'à ce que vous tentiez de repositionner l'enregistrement actif.

Si vous appelez la méthode **MoveLast** sur un objet **Recordset** contenant des enregistrements, le dernier enregistrement devient l'enregistrement actif ; si vous appelez ensuite la méthode **MoveNext**, l'enregistrement actif n'est plus valide et la propriété **EOF** a la valeur **True**. À l'inverse, si vous appelez la méthode **MoveFirst** sur un objet **Recordset** qui contient des enregistrements, le premier enregistrement devient l'enregistrement actif. Si vous utilisez ensuite la méthode **MovePrevious**, aucun enregistrement n'est actif et la propriété **BOF** prend la valeur **True**.

En règle générale, lorsque vous manipulez tous les enregistrements d'un objet **Recordset**, votre code parcourt tous les enregistrements à l'aide de la méthode **MoveNext** jusqu'à ce que la propriété **EOF** ait la valeur **True**.

Si vous appelez la méthode **MoveNext** alors que la propriété **EOF** a la valeur **True** ou la méthode **MovePrevious** alors que la propriété **BOF** a la valeur **True**, une erreur se produit.

Ce tableau indique les méthodes Move autorisées en fonction des différentes combinaisons des propriétés **BOF** et **EOF**.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Déplacer &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Déplacer &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = True,</strong><br />
<strong>EOF = False</strong></p></td>
<td><p>Autorisé</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
<td><p>Autorisé</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = False,</strong><br />
<strong>EOF = True</strong></p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
</tr>
<tr class="odd">
<td><p>Les deux propriétés ont la valeur <strong>True</strong></p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
</tr>
<tr class="even">
<td><p>Les deux propriétés ont la valeur <strong>False</strong></p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
</tr>
</tbody>
</table>


Si une méthode Move est autorisée, cela ne signifie pas qu'elle parviendra à localiser un enregistrement, mais simplement que la tentative d'exécution de la méthode Move est autorisée et qu'elle ne générera pas d'erreur. L'état des propriétés **BOF** et **EOF** peut changer à la suite de l'exécution de la méthode Move.

Une méthode **OpenRecordset** appelle en interne une méthode **MoveFirst**. Par conséquent, l'exécution d'une méthode **OpenRecordset** sur un jeu d'enregistrements vide affecte aux propriétés **BOF** et **EOF** la valeur **True** (consultez le tableau suivant pour en savoir plus sur le comportement d'une méthode **MoveFirst** qui a échoué).

Toutes les méthodes Move qui parviennent à localiser un enregistrement affectent aux propriétés **BOF** et **EOF** la valeur **False**.

Dans un espace de travail Microsoft Access, si vous ajoutez un enregistrement à un objet **Recordset** vide, **BOF** prend la valeur **False** mais **EOF** conserve la valeur **True**, indiquant que la fin de l'objet **Recordset** se trouve à la position actuelle.

L'appel de la méthode **Delete**, même si elle supprime le dernier enregistrement présent dans un objet **Recordset** ne modifie pas le paramètre des propriétés **BOF** ou **EOF**.

Le tableau suivant montre les répercussions sur les paramètres des propriétés **BOF** et **EOF** lorsque les méthodes Move ne parviennent pas à localiser un enregistrement.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td><p><strong>Move</strong> 0</p></td>
<td><p>Aucune modification</p></td>
<td><p>Aucune modification</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>déplacer</strong> &lt; 0</p></td>
<td><p><strong>True</strong></p></td>
<td><p>Aucune modification</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>déplacer</strong> &gt; 0</p></td>
<td><p>Aucune modification</p></td>
<td><p><strong>True</strong></p></td>
</tr>
</tbody>
</table>


---
title: Field2.ValidationRule, propriété (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3e2c8ba72f55f5c362e01726d0a528b12d9a9960
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552940"
---
# <a name="field2validationrule-property-dao"></a>Field2.ValidationRule, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui valide les données d'un champ lorsque ce dernier est modifié ou ajouté à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*.* ValidationRule

*expression* Expression qui renvoie un **objet Field2.**

## <a name="remarks"></a>Remarques

Les paramètres ou les valeurs de retour sont une chaîne qui décrit une comparaison sous la forme d'une clause SQL WHERE sans le mot réservé WHERE. Pour un objet pas encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture/écriture.

La propriété **ValidationRule** détermine si un champ contient ou non des données valides. Si les données ne sont pas valides, une erreur d'exécution capturable survient. Le message d'erreur renvoyé est le texte de la propriété **ValidationText**, s'il est spécifié, ou le texte de l'expression spécifié par **ValidationRule**.

Pour un objet **Field2**, l'utilisation de la propriété **ValidationRule** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field2** est ajouté.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objet ajouté à</p></th>
<th><p>Utilisation</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lecture/écriture</p></td>
</tr>
</tbody>
</table>


La validation est prise en charge uniquement pour les bases de données utilisant le moteur de base de données Microsoft Access.

L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field2** peut se référer uniquement à ce champ **Field2**. Elle ne peut pas se référer aux fonctions personnalisées, aux fonctions agrégées SQL ou aux requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field2** lorsque son paramètre de propriété **ValidateOnSet** est **True**, l'expression doit analyser avec succès (avec le nom du champ comme opérande implicite) et évaluer à **True**. Si son paramètre de propriété **ValidateOnSet** est **False**, le paramètre de propriété **ValidationRule** est ignoré.


> [!NOTE]
> Si vous définissez la propriété sur une chaîne concatentée avec une valeur non-integer, et que les paramètres système spécifient une valeur non américaine. caractère décimal tel qu’une virgule (par exemple, strRule = « PRICE &gt; " &amp; lngPrice et lngPrice = 125,50), une erreur se résulte lorsque votre code tente de valider des données. Ceci parce que pendant la concaténation, le nombre est converti en une chaîne à l'aide du caractère décimal par défaut de votre système et le moteur de base de données SQL Microsoft Access n'accepte que les caractères décimaux US.



---
title: Field. ValidationRule, propriété (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ef68db39b7dcad380eae16f789f4dd5b0eab75f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292943"
---
# <a name="fieldvalidationrule-property-dao"></a>Field. ValidationRule, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui valide les données d'un champ lorsque ce dernier est modifié ou ajouté à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . ValidationRule

*expression* Expression qui renvoie un objet **Field** .

## <a name="remarks"></a>Remarques

Les paramètres ou valeurs de retour sont des chaînes (type String) qui décrivent une comparaison sous la forme d'une clause SQL WHERE sans le mot réservé WHERE. Pour un objet non encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture/écriture.

La propriété **ValidationRule** détermine si un champ contient des données valides. Si les données ne sont pas valides, une erreur d'exécution interceptable se produit. Le message d'erreur renvoyé contient le texte de la propriété **[ValidationText](field-validationtext-property-dao.md)**, si elle est spécifiée, ou le texte de l'expression spécifiée par **ValidationRule**.

Pour un objet **[Field](field-object-dao.md)**, l'utilisation de la propriété **ValidationRule** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field** est ajouté.

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
<td><p>Non pris en charge</p></td>
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
<td><p>En lecture-écriture.</p></td>
</tr>
</tbody>
</table>


La validation n'est prise en charge que par les bases de données qui utilisent le moteur de base de données Microsoft Access.

L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field** ne peut faire référence qu'à cet objet **Field**. L'expression ne peut pas faire référence à des fonctions définies par l'utilisateur, à des fonctions d'agrégation SQL ni à des requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field** lorsque sa propriété **ValidateOnSet** a la valeur **True**, l'expression doit analyser avec succès (avec le nom du champ en tant qu'opérateur implicite) et être évaluée à **True**. Si sa propriété **ValidateOnSet** a la valeur **False**, la valeur de la propriété **ValidationRule** est ignorée.


> [!NOTE]
> Si vous définissez la propriété sur une chaîne concaténée avec une valeur non entière et que les paramètres système spécifient un caractère non-U. S. Decimal tel qu'une virgule (par exemple, strRule = "Price &gt; " &amp; lngPrice et lngPrice = 125, 50), une erreur se produit lorsque votre code tente de valider des données. Ceci parce que pendant la concaténation, le nombre est converti en une chaîne à l'aide du caractère décimal par défaut de votre système et le moteur de base de données SQL Microsoft Access n'accepte que les caractères décimaux US.



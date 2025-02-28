---
title: Recordset2.ValidationRule, propriété (DAO)
TOCTitle: ValidationRule Property
ms:assetid: d46cc255-e588-e9e6-66d7-31fc26ae45b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835002(v=office.15)
ms:contentKeyID: 48547940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9fb85f1fd071beb3184cd578db6aa3193ce93eca
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63723585"
---
# <a name="recordset2validationrule-property-dao"></a>Recordset2.ValidationRule, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui valide les données dans un champ au moment de leur modification ou de leur ajout à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*.* ValidationRule

*expression* Variable qui représente un **objet Recordset2** .

## <a name="remarks"></a>Remarques

Les paramètres ou valeurs de retour sont des chaînes (type **String**) qui décrivent une comparaison sous la forme d'une clause SQL WHERE sans le mot réservé WHERE. Pour un objet non encore ajouté à la collection **Fields**, cette propriété est en lecture/écriture.

La propriété **ValidationRule** détermine si un champ contient des données valides. Si ce n'est pas le cas, une erreur d'exécution piégeable se produit. Le message d'erreur renvoyé représente le texte de la propriété **ValidationText**, si cette propriété a été définie, ou le texte de l'expression spécifié par la propriété **ValidationRule**.

For a **Recordset** object, use of the **ValidationRule** property is read-only. For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>TableDef</p></th>
<th><p>Utilisation</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Table de base</p></td>
<td><p>Lecture/écriture</p></td>
</tr>
<tr class="even">
<td><p>Table liée</p></td>
<td><p>Lecture seule</p></td>
</tr>
</tbody>
</table>


La validation est uniquement prise en charge pour les bases de données qui utilisent le moteur de base de données Microsoft Access.

L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field** ne peut faire référence qu'à cet objet **Field**. L'expression ne peut pas faire référence à des fonctions définies par l'utilisateur, à des fonctions d'agrégation SQL ni à des requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field** lorsque sa propriété **ValidateOnSet** a la valeur **True**, l'expression doit analyser avec succès (avec le nom du champ en tant qu'opérateur implicite) et être évaluée à **True**. Si sa propriété **ValidateOnSet** a la valeur **False**, la valeur de la propriété **ValidationRule** est ignorée.

La propriété **ValidationRule** d'un objet **Recordset** ou **TableDef** peut référencer plusieurs champs de cet objet. Les restrictions mentionnées ci-dessus relatives à l'objet **Field** sont d'application.

Pour un objet **Recordset** de type table, la propriété **ValidationRule** hérite du paramètre de la propriété **ValidationRule** de l'objet **TableDef** utilisé pour créer l'objet **Recordset** de type table.

> [!NOTE]
> Si vous définissez la propriété sur une chaîne concatentée avec une valeur non-integer, et que les paramètres système spécifient une valeur non américaine. caractère décimal tel qu’une virgule (par exemple, strRule = « PRICE &gt; " &amp; lngPrice et lngPrice = 125,50), une erreur se résulte lorsque votre code tente de valider des données. En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</P>


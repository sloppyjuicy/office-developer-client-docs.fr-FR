---
title: Recordset.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: c9250c13-18fe-1ff7-7846-7872c49a1e3b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823208(v=office.15)
ms:contentKeyID: 48547671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a70dc412cbca420ca689fbd956e56d5bcdea556
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470723"
---
# <a name="recordsetvalidationrule-property-dao"></a>Recordset.ValidationRule Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Définit ou renvoie une valeur qui valide les données d'un champ pendant sa modification ou son ajout à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . ValidationRule (ValideSi)

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Les paramètres ou valeurs de retour sont de type **String**. Cette chaîne décrit une comparaison sous une forme similaire à une clause SQL WHERE sans le mot réservé WHERE. Pour un objet qui n'a pas encore été ajouté à la collection **Fields**, cette propriété est en lecture-écriture.

La propriété **ValidationRule** détermine si un champ contient des données valides. Si ce n'est pas le cas, une erreur d'exécution piégeable se produit. Le message d'erreur renvoyé représente le texte de la propriété **ValidationText**, si cette propriété a été définie, ou le texte de l'expression spécifié par la propriété **ValidationRule**.

Pour un objet **Recordset** , l’utilisation de la propriété **ValidationRule** est en lecture seule. Pour un objet **TableDef** , la propriété **ValidationRule** dépend de l’état de l’objet **TableDef** , comme le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td><p>En lecture-écriture</p></td>
</tr>
<tr class="even">
<td><p>Table liée</p></td>
<td><p>En lecture seule</p></td>
</tr>
</tbody>
</table>


La validation est uniquement prise en charge pour les bases de données qui utilisent le moteur de base de données Microsoft Access.

L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field** peut uniquement faire référence à cet objet **Field**. L'expression ne peut pas référencer des fonctions définies par l'utilisateur, des fonctions d'agrégation SQL ou des requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field** lorsque le paramètre de sa propriété **ValidateOnSet** est **True**, il doit être possible d'analyser l'expression (avec le nom du champ comme opérande implicite), laquelle doit correspondre à **True**. Si le paramètre de sa propriété **ValidateOnSet** est **False**, le paramètre de la propriété **ValidationRule** n'est pas pris en compte.

La propriété **ValidationRule** d'un objet **Recordset** ou **TableDef** peut référencer plusieurs champs de cet objet. Les restrictions mentionnées ci-dessus relatives à l'objet **Field** sont d'application.

Pour un objet **Recordset** de type table, la propriété **ValidationRule** hérite du paramètre de la propriété **ValidationRule** de l'objet **TableDef** utilisé pour créer l'objet **Recordset** de type table.


> [!NOTE]
> <P>Si vous définissez la propriété une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strRule = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque votre code tente de valider des données. En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</P>



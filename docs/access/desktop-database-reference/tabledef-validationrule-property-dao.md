---
title: TableDef.ValidationRule, propriété (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44329a4cc320e9adcc0612629bcc3fdcd179a1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314881"
---
# <a name="tabledefvalidationrule-property-dao"></a>TableDef.ValidationRule, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui valide les données dans un champ au moment de leur modification ou de leur ajout à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*.* ValidationRule

*expression* Variable représentant un objet **TableDef**.

## <a name="remarks"></a>Remarques

Les paramètres ou valeurs de retour sont des chaînes (type **String**) qui décrivent une comparaison sous la forme d'une clause SQL WHERE sans le mot réservé WHERE. Pour un objet non encore ajouté à la collection **Fields**, cette propriété est en lecture/écriture.

La propriété **ValidationRule** détermine si un champ contient des données valides. Si les données ne sont pas valides, une erreur d'exécution interceptable se produit. Le message d'erreur renvoyé contient le texte de la propriété **ValidationText**, si elle est spécifiée, ou le texte de l'expression spécifiée par **ValidationRule**.

La validation n'est prise en charge que par les bases de données qui utilisent le moteur de base de données Microsoft Access.

L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field** ne peut faire référence qu'à cet objet **Field**. L'expression ne peut pas faire référence à des fonctions définies par l'utilisateur, à des fonctions d'agrégation SQL ni à des requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field** lorsque sa propriété **ValidateOnSet** a la valeur **True**, l'expression doit analyser avec succès (avec le nom du champ en tant qu'opérateur implicite) et être évaluée à **True**. Si sa propriété **ValidateOnSet** a la valeur **False**, la valeur de la propriété **ValidationRule** est ignorée.

La propriété **ValidationRule** d'un objet **Recordset** ou **TableDef** peut faire référence à plusieurs champs dans cet objet. Les restrictions expliquées plus haut dans cette rubrique pour l'objet **Field** sont applicables.

Pour un objet **TableDef** basé sur une table liée, la propriété **ValidationRule** hérite de la valeur de la propriété **ValidationRule** de la table de base sous-jacente. Si celle table ne prend pas en charge la validation, la valeur de cette propriété est une chaîne nulle ("").

> [!NOTE]
> Si vous définissez la propriété sur une chaîne concatentée avec une valeur non-integer, et que les paramètres système spécifient une valeur non américaine. caractère décimal tel qu’une virgule (par exemple, strRule = « PRICE &gt; " &amp; lngPrice et lngPrice = 125,50), une erreur se résulte lorsque votre code tente de valider des données. En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.

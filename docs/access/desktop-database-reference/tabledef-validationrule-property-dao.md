---
title: TableDef.ValidationRule Property (DAO)
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
ms.openlocfilehash: cbcd456e2c3d64364a7c01ea71174999159f0aa4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881719"
---
# <a name="tabledefvalidationrule-property-dao"></a>TableDef.ValidationRule Property (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui valide les données d'un champ pendant sa modification ou son ajout à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . ValidationRule (ValideSi)

*expression* Variable qui représente un objet **TableDef** .

## <a name="remarks"></a>Remarques

Les paramètres ou valeurs de retour sont de type **String**. Cette chaîne décrit une comparaison sous une forme similaire à une clause SQL WHERE sans le mot réservé WHERE. Pour un objet qui n'a pas encore été ajouté à la collection **Fields**, cette propriété est en lecture-écriture.

La propriété **ValidationRule** détermine si un champ contient des données valides. Si les données ne sont pas valides, une erreur d'exécution interceptable se produit. Le message d'erreur renvoyé contient le texte de la propriété **ValidationText**, si elle est spécifiée, ou le texte de l'expression spécifiée par **ValidationRule**.

La validation n'est prise en charge que par les bases de données qui utilisent le moteur de base de données Microsoft Access.

L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field** peut uniquement faire référence à cet objet **Field**. L'expression ne peut pas référencer des fonctions définies par l'utilisateur, des fonctions d'agrégation SQL ou des requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field** lorsque le paramètre de sa propriété **ValidateOnSet** est **True**, il doit être possible d'analyser l'expression (avec le nom du champ comme opérande implicite), laquelle doit correspondre à **True**. Si le paramètre de sa propriété **ValidateOnSet** est **False**, le paramètre de la propriété **ValidationRule** n'est pas pris en compte.

La propriété **ValidationRule** d'un objet **Recordset** ou **TableDef** peut faire référence à plusieurs champs dans cet objet. Les restrictions expliquées plus haut dans cette rubrique pour l'objet **Field** sont applicables.

Pour un objet **TableDef** basé sur une table liée, la propriété **ValidationRule** hérite de la valeur de la propriété **ValidationRule** de la table de base sous-jacente. Si celle table ne prend pas en charge la validation, la valeur de cette propriété est une chaîne nulle ("").


> [!NOTE]
> <P>Si vous définissez la propriété une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strRule = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque votre code tente de valider des données. En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</P>



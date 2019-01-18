---
title: Propriété Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720085"
---
# <a name="field2expression-property-dao"></a>Propriété Field2.Expression (DAO)

**S’applique à**: Access 2013, Office 2013

Obtient ou définit une expression qui représente la formule pour un champ calculé. **String** en lecture/écriture.

## <a name="version-information"></a>Informations de version

Version ajoutée : Access 2010

## <a name="syntax"></a>Syntaxe

*expression* . Expression

*expression* Variable qui représente un objet **Field2** .

## <a name="remarks"></a>Remarques

Dans Access 2013, vous pouvez créer des champs de table calculer des valeurs. Les calculs peuvent inclure des valeurs de champs dans la même table, ainsi que les fonctions intégrées Access.

Le calcul ne peut pas inclure de champs à partir d’autres tables ou les requêtes.

Les résultats du calcul sont en lecture seule.

## <a name="example"></a>Exemple

L'exemple suivant montre comment créer un champ calculé. La méthode CreateField crée un champ nommé **FullName**. La propriété Expression est ensuite définie sur l'expression qui calcule la valeur du champ.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```


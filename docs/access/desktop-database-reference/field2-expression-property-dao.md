---
title: Field2.Expression, propriété (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 31a60ae12870b82cf6997b2afc03f149217c3de6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606701"
---
# <a name="field2expression-property-dao"></a>Field2.Expression, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Obtient ou définit une expression qui représente la formule d’un champ calculé. **String** en lecture/écriture.

## <a name="version-information"></a>Informations de version

Version ajoutée : Access 2010

## <a name="syntax"></a>Syntaxe

*.* Expression

*expression* une variable qui représente une **champ2** objet.

## <a name="remarks"></a>Remarques

Dans Access 2013, vous pouvez créer des champs de table qui calculent des valeurs. Les calculs peuvent inclure des valeurs provenant de champs de la même table, ainsi que des fonctions Access intégrées.

Le calcul ne peut pas inclure de champs provenant d’autres tables ou requêtes.

Les résultats du calcul sont en lecture seule.

## <a name="example"></a>Exemple

L'exemple suivant montre comment créer un champ calculé. La méthode CreateField crée un champ nommé **FullName**. La propriété Expression est ensuite définie sur l'expression qui calcule la valeur du champ.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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


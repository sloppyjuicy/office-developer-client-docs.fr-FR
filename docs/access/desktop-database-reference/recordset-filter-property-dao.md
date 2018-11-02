---
title: Propriété Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 94bb24fcd6df83f06a704c8569a1a6391638ad91
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923531"
---
# <a name="recordsetfilter-property-dao"></a>Propriété Recordset.Filter (DAO)

**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui détermine les enregistrements inclus dans un objet **Recordset** ouvert par la suite (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . Filtre

*expression* Expression qui renvoie un objet **Recordset** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données String qui contient une clause WHERE d'une instruction SQL sans le mot réservé WHERE.

Utilisez la propriété **Filter** pour appliquer un filtre à un objet **Recordset** de type avant uniquement, instantané ou feuille de réponse dynamique.

La propriété **Filter** permet de limiter le nombre d'enregistrements renvoyés à partir d'un objet existant lorsqu'un nouvel objet **Recordset** est ouvert sur la base d'un objet **Recordset** existant.

Utilisez le format de date américain (mois-jour-année) lorsque vous filtrez des champs contenant des dates, même si vous n’utilisez pas la version de moteur de base de données Microsoft Access (dans ce cas, vous devez assembler les dates en concaténant des chaînes, par exemple strMonth & «- » & strDay & «- » & strYear). Sinon, il est possible que le filtrage des données ne donne pas les résultats escomptés.

Dans la plupart des cas, il est plus rapide d'ouvrir un nouvel objet **Recordset** à l'aide d'une instruction SQL qui inclut une clause WHERE.

Si vous définissez la propriété une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strFilter = « prix \> » & lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez de Ouvrez le prochain **jeu d’enregistrements**. En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.

## <a name="example"></a>Exemple

L'exemple suivant montre comment utiliser la propriété Filter pour déterminer les enregistrements à inclure dans un Recordset ouvert par la suite.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```

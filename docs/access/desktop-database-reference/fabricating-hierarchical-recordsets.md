---
title: Fabrication de recordsets hiérarchiques
TOCTitle: Fabricating hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2cf3af43e288fc95bc7a8b21f90955f1061ac050
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552961"
---
# <a name="fabricating-hierarchical-recordsets"></a>Fabrication de recordsets hiérarchiques


**S’applique à** : Access 2013, Office 2013

L'exemple ci-après indique comment créer un jeu d'enregistrements hiérarchique sans source de données sous-jacente en utilisant la syntaxe de mise en forme des données pour définir les colonnes des objets **Recordset** parents, enfants ou petits-enfants.

Pour créer un **jeu d'enregistrements**, hiérarchique, vous devez spécifier le service de mise en forme des données Microsoft pour OLE DB (MSDataShape). Vous pouvez spécifier la valeur de fournisseur de données NONE dans le paramètre de chaîne de connexion de la méthode [Open](connection-object-ado.md) de l'objet [Connection](open-method-ado-connection.md) . Pour plus d'informations, reportez-vous à la section [Fournisseurs requis pour la mise en forme des données](required-providers-for-data-shaping.md).

```vb
    Dim cn As New ADODB.Connection
    Dim rsCustomers As New ADODB.Recordset
    
    cn.Open "Provider=MSDataShape;Data Provider=NONE;"
     
    strShape = _
    "SHAPE APPEND NEW adInteger AS CustID," & _
                " NEW adChar(25) AS FirstName," & _
                " NEW adChar(25) AS LastName," & _
                " NEW adChar(12) AS SSN," & _
                " NEW adChar(50) AS Address," & _
             " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                            " NEW adInteger AS CustID," & _
                            " NEW adChar(20) AS BodyColor, " & _
                         " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                                        " NEW adChar(20) AS Make, " & _
                                        " NEW adChar(20) AS Model," & _
                                        " NEW adChar(4) AS Year) " & _
                            " AS VINS RELATE VIN_NO TO VIN_NO))" & _
                " AS Vehicles RELATE CustID TO CustID) "
     
    rsCustomers.Open strShape, cn, adOpenStatic, adLockOptimistic, -1
```

Une fois **le recordset** fabriqué, il peut être rempli, manipulé ou persistant dans un fichier.


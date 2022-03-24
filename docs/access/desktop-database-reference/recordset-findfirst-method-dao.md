---
title: Recordset.FindFirst, méthode (DAO)
TOCTitle: FindFirst Method
ms:assetid: 5fcf78cd-7d2c-2e47-14e5-996f2e14ff51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194787(v=office.15)
ms:contentKeyID: 48545170
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 2e37ade2c8c227e42823a5cd267d73c25d58fa74
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725430"
---
# <a name="recordsetfindfirst-method-dao"></a>Recordset.FindFirst, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Localise le premier enregistrement dans un objet **Recordset** de type feuille de réponse dynamique ou capture instantanée qui remplit les critères spécifiés et rend l’enregistrement actif (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* .FindFirst(***Criteria***)

*expression* Variable représentant un objet **Recordset**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Critères</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Données de type String utilisées pour localiser l'enregistrement. S'apparente à la clause WHERE d'une instruction SQL sans toutefois le mot WHERE.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Si vous souhaitez inclure tous les enregistrements dans votre recherche, et non uniquement ceux qui remplissent une condition particulière, utilisez les méthodes **Move** pour passer d’un enregistrement à un autre. Pour localiser un enregistrement dans un **Recordset** de type table, utilisez la méthode **Seek**.

Si un enregistrement correspondant aux critères n’est pas localisé, le pointeur d’enregistrement actif est inconnu et la propriété **NoMatch** est définie sur **True**. Si le recordset contient plusieurs enregistrements correspondant aux critères, **FindFirst** localise la première occurrence, **FindNext** localise l’occurrence suivante, et ainsi de suite.

Chacune des méthodes **Find** commence sa recherche à partir de l’emplacement et dans le sens spécifiés dans le tableau suivant.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Méthode Find</p></th>
<th><p>Point de départ de la recherche</p></th>
<th><p>Sens de la recherche</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FindFirst</strong></p></td>
<td><p>Début du jeu d'enregistrements</p></td>
<td><p>Fin du jeu d’enregistrements</p></td>
</tr>
<tr class="even">
<td><p><strong>FindLast</strong></p></td>
<td><p>Fin du jeu d'enregistrements</p></td>
<td><p>Début du jeu d’enregistrements</p></td>
</tr>
<tr class="odd">
<td><p><strong>FindNext</strong></p></td>
<td><p>Enregistrement actif</p></td>
<td><p>Fin du jeu d'enregistrements</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>Enregistrement actif</p></td>
<td><p>Début du jeu d'enregistrements</p></td>
</tr>
</tbody>
</table>

L’utilisation de l’une des méthodes **Find** n’équivaut pas à utiliser une méthode **Move**, qui ne fait que rendre actif l’enregistrement initial, final, suivant ou précédent sans spécifier de condition. Vous pouvez faire suivre une opération Find d’une opération Move.

Vérifiez toujours la valeur de la propriété **NoMatch** pour déterminer si l’opération Find a réussi. Si la recherche aboutit, **NoMatch** a la valeur **False**. Si elle échoue, **NoMatch** a la valeur **True** et l’enregistrement actif n’est pas défini. Dans ce cas, vous devez positionner le pointeur d’enregistrement actif sur un enregistrement valide.

L’utilisation des méthodes **Find** avec les recordsets ODBC connectés au moteur de base de données Microsoft Access peut s’avérer inefficace. Il se peut que la reformulation de vos critères pour localiser un enregistrement spécifique soit plus rapide, surtout si vous travaillez avec des recordsets volumineux.

Lorsque vous utilisez des bases de données ODBC connectées au moteur de base de données Microsoft Access et de grands objets **Recordset** de type feuille de réponse dynamique, il se peut que l’utilisation des méthodes **Find** ou des propriétés **Sort** ou **Filter** soit lente. Pour améliorer les performances, utilisez des requêtes SQL avec des clauses ORDER BY ou WHERE personnalisées, des requêtes avec paramètres ou des objets **QueryDef** qui récupèrent des enregistrements indexés spécifiques.

Vous devez utiliser un format de date américain (mois-jour-année) lorsque vous recherchez des champs contenant des dates, même si vous n’utilisez pas la version américaine du moteur de base de données Microsoft Access. Sinon, les données risquent de ne pas être trouvées. Utilisez la fonction **Format** de Visual Basic pour convertir la date. Par exemple :

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Si les critères sont composés d’une chaîne concaténée avec une valeur non entière, et que les paramètres système indiquent un caractère décimal non américain, comme une virgule (par exemple, strSQL = "PRICE \> " & lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous tentez d’appeler la méthode. Ceci est dû au fait que, lors de la concaténation, le nombre sera converti en chaîne à l’aide du caractère décimal par défaut de votre système, et Microsoft Access SQL accepte uniquement les caractères décimaux américains.

> [!NOTE]
> Pour des performances optimales, les *critères* doivent être au format «*champ* = *valeur*» où *champ* est un champ indexé dans la table de base sous-jacente, ou au format «*champ* LIKE *préfixe*» où *champ* est un champ indexé dans la table de base sous-jacente et *préfixe* une chaîne de recherche de préfixe (par exemple, « ART* »).
>
> En général, pour des types de recherches équivalents, la méthode **Seek** offre de meilleures performances que les méthodes **Find**. Cela suppose que les objets **Recordset** de type table suffisent à répondre à vos besoins.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser les méthodes TrouverPremier et TrouverSuivant pour rechercher un enregistrement dans un Recordset.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

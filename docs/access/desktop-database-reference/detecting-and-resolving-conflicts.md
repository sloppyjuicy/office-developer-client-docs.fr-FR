---
title: Détection et résolution des conflits
TOCTitle: Detecting and resolving conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ddd7566be2581fe449872eb576bf7f11e5a806fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716626"
---
# <a name="detecting-and-resolving-conflicts"></a>Détection et résolution des conflits

**S’applique à**: Access 2013, Office 2013

## <a name="detecting-and-resolving-conflicts"></a>Détection et résolution des conflits

Si vous manipulez votre objet **Recordset** en mode de mise à jour immédiate, les problèmes d'accès concurrentiel sont fortement réduits. En revanche, si votre application utilise le mode de mise à jour par lot, il est fort probable qu'un utilisateur modifie un enregistrement avant que des modifications apportées par un autre utilisateur à ce même enregistrement soient enregistrées. Dans une tel cas, vous pouvez souhaiter que l'application gère correctement le conflit. Vous voulez peut-être que la dernière personne à avoir envoyé une mise à jour au serveur « gagne » ou que le dernier utilisateur décide de la mise à jour prioritaire en lui donnant le choix entre les deux valeurs conflictuelles.

Quoi qu'il en soit, ADO fournit les propriétés **UnderlyingValue** et **OriginalValue** de l'objet **Field** afin de gérer ces types de conflits. Utilisez ces propriétés avec la méthode **Resync** et la propriété **Filter** de l'objet **Recordset**.

## <a name="detecting-errors"></a>Détection des erreurs

En cas de conflit détecté par ADO au cours d'une mise à jour par lot, un avertissement est placé dans la collection **Errors**. Par conséquent, vous devez toujours contrôler les erreurs immédiatement après un appel de **BatchUpdate**, et si vous en trouvez, vous devez vérifier s'il s'agit effectivement d'un conflit. Vous devez d'abord affecter à la propriété **Filter** de l'objet **Recordset** la valeur **adFilterConflictingRecords** (la propriété **Filter** est décrite dans le chapitre précédent). De cette façon, seuls les enregistrements conflictuels sont affichés dans votre objet **Recordset**. Si la propriété **RecordCount** est égale à zéro une fois cette étape franchie, vous pouvez en déduire que la cause de l'erreur n'est pas un conflit.

Lorsque vous appelez **BatchUpdate**, ADO et le fournisseur génèrent des instructions SQL pour effectuer des mises à jour sur la source de données. N'oubliez pas que certaines sources de données possèdent des restrictions quant aux types de colonnes autorisés dans une clause WHERE.

Ensuite, appelez la méthode **Resync** sur le **jeu d’enregistrements** avec l’argument *AffectRecords* égal à **adAffectGroup** et l’argument *ResyncValues* égal à **adResyncUnderlyingValues**. La méthode **Resync** actualise les données dans l'objet **Recordset** actif à partir de la base de données sous-jacente. Si vous utilisez **adAffectGroup**, seuls les enregistrements visibles avec le paramètre de filtre actuel, à savoir les enregistrements présentant un conflit, sont resynchronisés avec la base de données. Ceci permet d'améliorer sensiblement les performances lorsque vous travaillez avec un objet **Recordset** volumineux. En définissant l’argument *ResyncValues* **adResyncUnderlyingValues** lors de l’appel de **Resync**, vous assurez que la propriété **UnderlyingValue** contiendra la valeur (conflictuelle) de la base de données que la **valeur** propriété conserve la valeur saisie par l’utilisateur, et que la propriété **OriginalValue** doit contenir la valeur d’origine pour le champ (la valeur qu’il avait avant le dernier appel réussi de **UpdateBatch** a été effectué). Vous pouvez alors utiliser ces valeurs pour résoudre le conflit par programme ou demander à l'utilisateur de choisir la valeur à utiliser.

Cette technique est illustrée dans l'exemple de code suivant. Un conflit y est artificiellement créé en utilisant un objet **Recordset** distinct pour modifier une valeur dans la table sous-jacente avant l'appel de **UpdateBatch**.

```vb 
 
'BeginConflicts 
    On Error GoTo ErrHandler: 
     
    Dim objRs1 As New ADODB.Recordset 
    Dim objRs2 As New ADODB.Recordset 
    Dim strSQL As String 
    Dim strMsg As String 
     
    strSQL = "SELECT * FROM Shippers WHERE ShipperID = 2" 
                  
    'Open Rs and change a value 
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
    objRs1("Phone") = "(111) 555-1111" 
     
    'Introduce a conflict at the db... 
    objRs2.Open strSQL, strConn, adOpenKeyset, adLockOptimistic, adCmdText 
    objRs2("Phone") = "(999) 555-9999" 
    objRs2.Update 
    objRs2.Close 
    Set objRs2 = Nothing 
     
    On Error Resume Next 
    objRs1.UpdateBatch 
     
    If objRs1.ActiveConnection.Errors.Count <> 0 Then 
        Dim intConflicts As Integer 
         
        intConflicts = 0 
         
        objRs1.Filter = adFilterConflictingRecords 
         
        intConflicts = objRs1.RecordCount 
         
        'Resync so we can see the UnderlyingValue and offer user a choice. 
        'This sample only displays all three values and resets to original. 
        objRs1.Resync adAffectGroup, adResyncUnderlyingValues 
         
        If intConflicts > 0 Then 
            strMsg = "A conflict occurred with updates for " & intConflicts & _ 
                     " record(s)." & vbCrLf & "The values will be restored" & _ 
                     " to their original values." & vbCrLf & vbCrLf 
                      
            objRs1.MoveFirst 
            While Not objRs1.EOF 
                strMsg = strMsg & "SHIPPER = " & objRs1("CompanyName") & vbCrLf 
                strMsg = strMsg & "Value = " & objRs1("Phone").Value & vbCrLf 
                strMsg = strMsg & "UnderlyingValue = " & _ 
                                   objRs1("Phone").UnderlyingValue & vbCrLf 
                strMsg = strMsg & "OriginalValue = " & _ 
                                   objRs1("Phone").OriginalValue & vbCrLf 
                strMsg = strMsg & vbCrLf & "Original value has been restored." 
                   
                MsgBox strMsg, vbOKOnly, _ 
                      "Conflict " & objRs1.AbsolutePosition & _ 
                      " of " & intConflicts 
                   
                objRs1("Phone").Value = objRs1("Phone").OriginalValue 
                objRs1.MoveNext 
            Wend 
             
            objRs1.UpdateBatch adAffectGroup 
        Else 
            'Other error occurred. Minimal handling in this example. 
             strMsg = "Errors occurred during the update. " & _ 
                        objRs1.ActiveConnection.Errors(0).Number & " " & _ 
                        objRs1.ActiveConnection.Errors(0).Description 
        End If 
         
        On Error GoTo 0 
    End If 
     
    objRs1.MoveFirst 
     
    'Clean up 
    objRs1.Close 
    Set objRs1 = Nothing 
    Exit Sub 
     
ErrHandler: 
    
    If Not objRs1 Is Nothing Then 
        If objRs1.State = adStateOpen Then objRs1.Close 
        Set objRs1 = Nothing 
    End If 
     
    If Not objRs2 Is Nothing Then 
        If objRs2.State = adStateOpen Then objRs2.Close 
        Set objRs2 = Nothing 
    End If 
     
    If Err <> 0 Then 
        MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
     
'EndConflicts 
```

Vous pouvez utiliser la propriété **Status** de l'objet **Record** actif ou d'un objet **Field** spécifique pour déterminer le type de conflit en cours.

Pour plus d'informations sur la gestion des erreurs, consultez le [chapitre 6 : Gestion des erreurs](chapter-6-error-handling.md).


---
title: Détection et résolution des conflits
TOCTitle: Detecting and Resolving Conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76bfc8f81b7f9df3d1b0e759620952f92bb5c8f1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875293"
---
# <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="d9a7b-102">Détection et résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="d9a7b-102">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="d9a7b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9a7b-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="d9a7b-104">Détection et résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="d9a7b-104">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="d9a7b-p101">Si vous manipulez votre objet **Recordset** en mode de mise à jour immédiate, les problèmes d'accès concurrentiel sont fortement réduits. En revanche, si votre application utilise le mode de mise à jour par lot, il est fort probable qu'un utilisateur modifie un enregistrement avant que des modifications apportées par un autre utilisateur à ce même enregistrement soient enregistrées. Dans une tel cas, vous pouvez souhaiter que l'application gère correctement le conflit. Vous voulez peut-être que la dernière personne à avoir envoyé une mise à jour au serveur « gagne » ou que le dernier utilisateur décide de la mise à jour prioritaire en lui donnant le choix entre les deux valeurs conflictuelles.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-p101">If you are dealing with your **Recordset** in immediate mode, there is much less chance for concurrency problems to arise. On the other hand, if your application uses batch mode updating, there may be a good chance that one user will change a record before changes made by another user editing the same record are saved. In such a case, you will want your application to gracefully handle the conflict. It may be your wish that the last person to send an update to the server "wins." Or you may want to let the most recent user to decide which update should take precedence by providing him with a choice between the two conflicting values.</span></span>

<span data-ttu-id="d9a7b-p102">Quoi qu'il en soit, ADO fournit les propriétés **UnderlyingValue** et **OriginalValue** de l'objet **Field** afin de gérer ces types de conflits. Utilisez ces propriétés avec la méthode **Resync** et la propriété **Filter** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-p102">Whatever the case, ADO provides the **UnderlyingValue** and **OriginalValue** properties of the **Field** object in order to handle these types of conflicts. Use these properties in combination with the **Resync** method and **Filter** property of the **Recordset**.</span></span>

## <a name="detecting-errors"></a><span data-ttu-id="d9a7b-112">Détection des erreurs</span><span class="sxs-lookup"><span data-stu-id="d9a7b-112">Detecting Errors</span></span>

<span data-ttu-id="d9a7b-p103">En cas de conflit détecté par ADO au cours d'une mise à jour par lot, un avertissement est placé dans la collection **Errors**. Par conséquent, vous devez toujours contrôler les erreurs immédiatement après un appel de **BatchUpdate**, et si vous en trouvez, vous devez vérifier s'il s'agit effectivement d'un conflit. Vous devez d'abord affecter à la propriété **Filter** de l'objet **Recordset** la valeur **adFilterConflictingRecords** (la propriété **Filter** est décrite dans le chapitre précédent). De cette façon, seuls les enregistrements conflictuels sont affichés dans votre objet **Recordset**. Si la propriété **RecordCount** est égale à zéro une fois cette étape franchie, vous pouvez en déduire que la cause de l'erreur n'est pas un conflit.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-p103">When ADO encounters a conflict during a batch update, a warning will be placed in the **Errors** collection. Therefore, you should always check for errors immediately after calling **BatchUpdate**, and if you find them, begin testing the assumption that you have encountered a conflict. The first step is to set the **Filter** property on the **Recordset** equal to **adFilterConflictingRecords** (the **Filter** property is discussed in the preceding chapter). This limits the view on your **Recordset** to only those records that are in conflict. If the **RecordCount** property is equal to zero after this step, you know the error was raised by something other than a conflict.</span></span>

<span data-ttu-id="d9a7b-p104">Lorsque vous appelez **BatchUpdate**, ADO et le fournisseur génèrent des instructions SQL pour effectuer des mises à jour sur la source de données. N'oubliez pas que certaines sources de données possèdent des restrictions quant aux types de colonnes autorisés dans une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-p104">When you call **BatchUpdate**, ADO and the provider are generating SQL statements to perform updates on the data source. Remember that certain data sources have limitations on which types of columns can be used in a WHERE clause.</span></span>

<span data-ttu-id="d9a7b-120">Ensuite, appelez la méthode **Resync** sur le **jeu d’enregistrements** avec l’argument *AffectRecords* égal à **adAffectGroup** et l’argument *ResyncValues* égal à **adResyncUnderlyingValues**.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-120">Next, call the **Resync** method on the **Recordset** with the *AffectRecords* argument set equal to **adAffectGroup** and the *ResyncValues* argument set equal to **adResyncUnderlyingValues**.</span></span> <span data-ttu-id="d9a7b-121">La méthode **Resync** actualise les données dans l'objet **Recordset** actif à partir de la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-121">The **Resync** method refreshes the data in the current **Recordset** object from the underlying database.</span></span> <span data-ttu-id="d9a7b-122">Si vous utilisez **adAffectGroup**, seuls les enregistrements visibles avec le paramètre de filtre actuel, à savoir les enregistrements présentant un conflit, sont resynchronisés avec la base de données.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-122">By using **adAffectGroup**, you are ensuring that only the records visible with the current filter setting, that is, only the conflicting records, are resynchronized with the database.</span></span> <span data-ttu-id="d9a7b-123">Ceci permet d'améliorer sensiblement les performances lorsque vous travaillez avec un objet **Recordset** volumineux.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-123">This could make a significant performance difference if you are dealing with a large **Recordset**.</span></span> <span data-ttu-id="d9a7b-124">En définissant l’argument *ResyncValues* **adResyncUnderlyingValues** lors de l’appel de **Resync**, vous assurez que la propriété **UnderlyingValue** contiendra la valeur (conflictuelle) de la base de données que la **valeur** propriété conserve la valeur saisie par l’utilisateur, et que la propriété **OriginalValue** doit contenir la valeur d’origine pour le champ (la valeur qu’il avait avant le dernier appel réussi de **UpdateBatch** a été effectué).</span><span class="sxs-lookup"><span data-stu-id="d9a7b-124">By setting the *ResyncValues* argument to **adResyncUnderlyingValues** when calling **Resync**, you ensure that the **UnderlyingValue** property will contain the (conflicting) value from the database, that the **Value** property will maintain the value entered by the user, and that the **OriginalValue** property will hold the original value for the field (the value it had before the last successful **UpdateBatch** call was made).</span></span> <span data-ttu-id="d9a7b-125">Vous pouvez alors utiliser ces valeurs pour résoudre le conflit par programme ou demander à l'utilisateur de choisir la valeur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-125">You can then use these values to resolve the conflict programmatically or require the user to choose the value that will be used.</span></span>

<span data-ttu-id="d9a7b-p106">Cette technique est illustrée dans l'exemple de code suivant. Un conflit y est artificiellement créé en utilisant un objet **Recordset** distinct pour modifier une valeur dans la table sous-jacente avant l'appel de **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-p106">This technique is shown in the code example below. The example artificially creates a conflict by using a separate **Recordset** to change a value in the underlying table before **UpdateBatch** is called.</span></span>

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

<span data-ttu-id="d9a7b-128">Vous pouvez utiliser la propriété **Status** de l'objet **Record** actif ou d'un objet **Field** spécifique pour déterminer le type de conflit en cours.</span><span class="sxs-lookup"><span data-stu-id="d9a7b-128">You can use the **Status** property of the current **Record** or of a specific **Field** to determine what kind of a conflict has occurred.</span></span>

<span data-ttu-id="d9a7b-129">Pour plus d'informations sur la gestion des erreurs, consultez le [chapitre 6 : Gestion des erreurs](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="d9a7b-129">For more detailed information on error handling, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>


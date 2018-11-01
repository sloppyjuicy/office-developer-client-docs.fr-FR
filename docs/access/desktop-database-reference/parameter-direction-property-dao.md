---
title: Parameter.Direction Property (DAO)
TOCTitle: Direction Property
ms:assetid: b78c87ff-1181-21ef-7126-92d309751005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822422(v=office.15)
ms:contentKeyID: 48547300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053586
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c06fbf6bb3424e776e21f32343c8cdb8a795b604
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877106"
---
# <a name="parameterdirection-property-dao"></a><span data-ttu-id="8bcc8-102">Parameter.Direction Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="8bcc8-102">Parameter.Direction Property (DAO)</span></span>


<span data-ttu-id="8bcc8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bcc8-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="syntax"></a><span data-ttu-id="8bcc8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bcc8-104">Syntax</span></span>

<span data-ttu-id="8bcc8-105">*expression* . Direction</span><span class="sxs-lookup"><span data-stu-id="8bcc8-105">*expression* .Direction</span></span>

<span data-ttu-id="8bcc8-106">*expression* Variable qui représente un objet **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="8bcc8-106">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bcc8-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="8bcc8-107">Remarks</span></span>

<span data-ttu-id="8bcc8-108">Le paramètre ou la valeur de retour est une valeur longue pouvant être définie sur l'une des constantes **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8bcc8-108">The setting or return value is a Long that can be set to one of the **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="8bcc8-p101">La propriété **Direction** permet de déterminer si le paramètre est un paramètre d'entrée, de sortie, ou les deux, ou la valeur de retour de la procédure. Certains pilotes ODBC ne fournissent aucune information sur la direction des paramètres vers une instruction SELECT ou une invocation de procédure. Dans ce cas, il convient de définir la direction avant d'exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="8bcc8-p101">Use the **Direction** property to determine whether the parameter is an input parameter, output parameter, both, or the return value from the procedure. Some ODBC drivers do not provide information on the direction of parameters to a SELECT statement or procedure call. In these cases, it is necessary to set the direction prior to executing the query.</span></span>

<span data-ttu-id="8bcc8-112">Par exemple, la procédure suivante renvoie une valeur à partir d’une procédure stockée appelée « obtenir\_employés » :</span><span class="sxs-lookup"><span data-stu-id="8bcc8-112">For example, the following procedure returns a value from a stored procedure named "get\_employees":</span></span>

<span data-ttu-id="8bcc8-113">{?</span><span class="sxs-lookup"><span data-stu-id="8bcc8-113"></span></span> <span data-ttu-id="8bcc8-114">= appel get\_employés}</span><span class="sxs-lookup"><span data-stu-id="8bcc8-114">= call get\_employees}</span></span>

<span data-ttu-id="8bcc8-p103">Cet appel produit un paramètre : la valeur de retour. Vous devez définir la direction de ce paramètre sur **dbParamOutput** ou **dbParamReturnValue** avant d'exécuter l'objet **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8bcc8-p103">This call produces one parameter — the return value. You need to set the direction of this parameter to **dbParamOutput** or **dbParamReturnValue** before executing the **[QueryDef](querydef-object-dao.md)**.</span></span>

<span data-ttu-id="8bcc8-117">Vous devez définir toutes les directions de paramètre sauf **dbParamInput** avant d'accéder aux valeurs des paramètres ou de les définir et avant d'exécuter l'objet **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="8bcc8-117">You need to set all parameter directions except **dbParamInput** before accessing or setting the values of the parameters and before executing the **QueryDef**.</span></span>

<span data-ttu-id="8bcc8-118">Utilisez **dbParamReturnValue** pour les valeurs de retour, mais dans les cas où cette option n'est pas prise en charge par le pilote ou le serveur, utilisez plutôt **dbParamOutput**.</span><span class="sxs-lookup"><span data-stu-id="8bcc8-118">You should use **dbParamReturnValue** for return values, but in cases where that option is not supported by the driver or the server, you can use **dbParamOutput** instead.</span></span>

<span data-ttu-id="8bcc8-p104">Le pilote Microsoft SQL Server définit automatiquement la propriété **Direction** pour tous les paramètres de procédure. Certains pilotes ODBC ne peuvent pas déterminer la direction d'un paramètre de requête. Dans ce cas, il convient de définir la direction avant d'exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="8bcc8-p104">The Microsoft SQL Server driver automatically sets the **Direction** property for all procedure parameters. Not all ODBC drivers can determine the direction of a query parameter. In these cases, it is necessary to set the direction prior to executing the query.</span></span>

## <a name="example"></a><span data-ttu-id="8bcc8-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="8bcc8-122">Example</span></span>

<span data-ttu-id="8bcc8-123">Cet exemple utilise la propriété **Direction** pour configurer les paramètres d'une requête sur une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="8bcc8-123">This example uses the **Direction** property to configure the parameters of a query to an ODBC data source.</span></span>

```vb 
Sub DirectionX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim strSQL As String 
 Dim intLoop As Integer 
 
 ' Create ODBC workspace and open a connection to a 
 ' Microsoft SQL Server database. 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Set SQL string to call the stored procedure 
 ' getempsperjob. 
 strSQL = "{ call getempsperjob (?, ?) }" 
 
 Set qdfTemp = conMain.CreateQueryDef("", strSQL) 
 
 With qdfTemp 
 ' Indicate that the two query parameters will only 
 ' pass information to the stored procedure. 
 .Parameters(0).Direction = dbParamInput 
 .Parameters(1).Direction = dbParamInput 
 
 ' Assign initial parameter values. 
 .Parameters(0) = "0877" 
 .Parameters(1) = 0 
 
 Set rstTemp = .OpenRecordset() 
 
 With rstTemp 
 ' Loop through all valid values for the second 
 ' parameter. For each value, requery the recordset 
 ' to obtain the correct results and then print out 
 ' the contents of the recordset. 
 For intLoop = 1 To 14 
 qdfTemp.Parameters(1) = intLoop 
 .Requery 
 Debug.Print "Publisher = " & _ 
 qdfTemp.Parameters(0) & _ 
 ", job = " & intLoop 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 Next intLoop 
 .Close 
 End With 
 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```


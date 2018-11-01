---
title: DBEngine.RegisterDatabase Method (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fcb8e675f488c0d69f4c0d0b6329c47085d51e26
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888621"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="3edaa-102">DBEngine.RegisterDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="3edaa-102">DBEngine.RegisterDatabase Method (DAO)</span></span>


<span data-ttu-id="3edaa-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3edaa-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3edaa-p101">Entre les informations de connexion pour une source de données ODBC dans le Registre Windows. Le pilote ODBC a besoin des informations de connexion lorsque la source de données ODBC est ouverte au cours d'une session.</span><span class="sxs-lookup"><span data-stu-id="3edaa-p101">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="3edaa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3edaa-106">Syntax</span></span>

<span data-ttu-id="3edaa-107">*expression* . RegisterDatabase (***Dsn***, ***pilote***, ***en mode silencieux***, ***attributs***)</span><span class="sxs-lookup"><span data-stu-id="3edaa-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="3edaa-108">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="3edaa-108">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="3edaa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3edaa-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3edaa-110">Name</span><span class="sxs-lookup"><span data-stu-id="3edaa-110">Name</span></span></p></th>
<th><p><span data-ttu-id="3edaa-111">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="3edaa-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="3edaa-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="3edaa-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="3edaa-113">Description</span><span class="sxs-lookup"><span data-stu-id="3edaa-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3edaa-114">DSN</span><span class="sxs-lookup"><span data-stu-id="3edaa-114">Dsn</span></span></p></td>
<td><p><span data-ttu-id="3edaa-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3edaa-115">Required</span></span></p></td>
<td><p><span data-ttu-id="3edaa-116"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="3edaa-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="3edaa-p102">Nom utilisé dans la méthode <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong>. Il désigne un bloc d’informations descriptives se rapportant à la source de données. Par exemple, si la source de données est une base de données distante ODBC, il peut s’agir du nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="3edaa-p102">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method. It refers to a block of descriptive information about the data source. For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edaa-120">Pilote</span><span class="sxs-lookup"><span data-stu-id="3edaa-120">Driver</span></span></p></td>
<td><p><span data-ttu-id="3edaa-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3edaa-121">Required</span></span></p></td>
<td><p><span data-ttu-id="3edaa-122"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="3edaa-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="3edaa-p103">Nom du pilote ODBC. Il ne s'agit pas du fichier DLL du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="3edaa-p103">The name of the ODBC driver. This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edaa-125">En mode silencieux</span><span class="sxs-lookup"><span data-stu-id="3edaa-125">Silent</span></span></p></td>
<td><p><span data-ttu-id="3edaa-126">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3edaa-126">Required</span></span></p></td>
<td><p><span data-ttu-id="3edaa-127"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="3edaa-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="3edaa-128"><strong>True</strong> si vous ne souhaitez pas afficher les boîtes de dialogue de pilote ODBC qui demandent des informations spécifiques au pilote ; ou <strong>False</strong> si vous souhaitez afficher les boîtes de dialogue du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="3edaa-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="3edaa-129">Si en mode silencieux a la <strong>valeur True</strong>, les attributs doivent contenir toutes les informations spécifiques au pilote nécessaires ou les boîtes de dialogue sont affichées.</span><span class="sxs-lookup"><span data-stu-id="3edaa-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edaa-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="3edaa-130">Attributes</span></span></p></td>
<td><p><span data-ttu-id="3edaa-131">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3edaa-131">Required</span></span></p></td>
<td><p><span data-ttu-id="3edaa-132"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="3edaa-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="3edaa-p105">Liste de mots clés à ajouter au registre Windows. Les mots clés se trouvent dans une chaîne délimitée par des retours chariot.</span><span class="sxs-lookup"><span data-stu-id="3edaa-p105">A list of keywords to be added to the Windows Registry. The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3edaa-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="3edaa-135">Remarks</span></span>

<span data-ttu-id="3edaa-136">Si la base de données est déjà enregistrée (les informations de connexion sont déjà entrées) dans le registre Windows lorsque vous utilisez la méthode **RegisterDatabase**, les informations de connexion sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="3edaa-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="3edaa-137">Si la méthode **RegisterDatabase** échoue pour une raison ou une autre, aucune modification n'est apportée au registre Windows, et une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="3edaa-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="3edaa-138">Pour plus d'informations sur les pilotes ODBC comme SQL Server, reportez-vous au fichier d'aide fourni avec le pilote.</span><span class="sxs-lookup"><span data-stu-id="3edaa-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="3edaa-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="3edaa-139">Example</span></span>

<span data-ttu-id="3edaa-140">Cet exemple utilise la méthode **RegisterDatabase** pour enregistrer une source de données Microsoft SQL Server appelée Éditeurs dans le registre Windows.</span><span class="sxs-lookup"><span data-stu-id="3edaa-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```


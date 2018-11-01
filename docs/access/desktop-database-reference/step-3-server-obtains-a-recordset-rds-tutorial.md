---
title: 'Étape 3 : le serveur obtient un objet Recordset (didacticiel RDS)'
TOCTitle: 'Step 3: Server Obtains a Recordset (RDS Tutorial)'
ms:assetid: fadb6a9b-ed44-264f-22fd-26b121f98040
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250282(v=office.15)
ms:contentKeyID: 48548856
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9f3299892118d044bfcc36f3fa28e4e25eaed9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881131"
---
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a><span data-ttu-id="92a13-102">Étape 3 : Le serveur obtient un recordset (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="92a13-102">Step 3: Server Obtains a Recordset (RDS Tutorial)</span></span>


<span data-ttu-id="92a13-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92a13-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92a13-p101">Le programme serveur utilise la chaîne de connexion et le texte de commande pour interroger la source de données et obtenir les lignes souhaitées. ADO est généralement utilisé pour récupérer cet objet **Recordset** même s'il est possible d'utiliser d'autres interfaces d'accès aux données Microsoft, comme OLE DB.</span><span class="sxs-lookup"><span data-stu-id="92a13-p101">The server program uses the connect string and command text to query the data source for the desired rows. ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="92a13-106">Un programme serveur personnalisé peut ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="92a13-106">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```


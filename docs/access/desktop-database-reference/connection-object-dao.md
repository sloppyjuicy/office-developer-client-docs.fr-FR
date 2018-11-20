---
title: Objet Connection (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95f70c233fdb299aa66c1cbeab9f5c27356c1e93
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026455"
---
# <a name="connection-object-dao"></a><span data-ttu-id="5728e-102">Objet Connection (DAO)</span><span class="sxs-lookup"><span data-stu-id="5728e-102">Connection object (DAO)</span></span>

<span data-ttu-id="5728e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5728e-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="5728e-p101">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5728e-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="5728e-106">Un objet **Connection** représente une connexion à une base de données ODBC (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="5728e-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="5728e-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="5728e-107">Remarks</span></span>

<span data-ttu-id="5728e-p102">Un objet **Connection** est un objet non persistant, qui représente une connexion à une base de données distante. L'objet **Connection** n'est disponible que dans les espaces de travail ODBCDirect (c'est-à-dire un objet **Workspace** créé avec l'option de type définie sur **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="5728e-p102">A **Connection** is a non-persistent object that represents a connection to a remote database. The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>

> [!NOTE]
> <span data-ttu-id="5728e-p103">[!REMARQUE] Le code écrit pour des versions antérieures de DAO peut continuer à utiliser l'objet **Database** pour la rétrocompatibilité, mais si les nouvelles caractéristiques d'un objet **Connection** sont souhaitées, vous devez réviser le code de manière à utiliser l'objet **Connection**. Pour vous aider avec la conversion du code, vous pouvez obtenir une référence d'objet **Connection** à partir d'un objet **Database** en lisant la propriété [Connection](database-connection-property-dao.md) de l'objet **Database**. À l'inverse, vous pouvez obtenir une référence d'objet **Database** à partir de la propriété **Database** de l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="5728e-p103">Code written for earlier versions of DAO can continue to use the **Database** object for backward compatibility, but if the new features of a **Connection** are desired, you should revise code to use the **Connection** object. To help with code conversion, you can obtain a **Connection** object reference from a **Database** by reading the [Connection](database-connection-property-dao.md) property of the **Database** object. Conversely, you can obtain a **Database** object reference from the **Connection** object's **Database** property.</span></span>



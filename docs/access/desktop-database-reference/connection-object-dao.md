---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bba06d593069051d2cc4f2e66b8cb91f36d920fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469887"
---
# <a name="connection-object-dao"></a><span data-ttu-id="932b5-102">Connection Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="932b5-102">Connection Object (DAO)</span></span>


<span data-ttu-id="932b5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="932b5-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <P><span data-ttu-id="932b5-p101">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="932b5-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>



<span data-ttu-id="932b5-106">Un objet **Connection** représente une connexion à une base de données ODBC (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="932b5-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="932b5-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="932b5-107">Remarks</span></span>

<span data-ttu-id="932b5-p102">Un objet **Connection** est un objet non persistant, qui représente une connexion à une base de données distante. L'objet **Connection** n'est disponible que dans les espaces de travail ODBCDirect (c'est-à-dire un objet **Workspace** créé avec l'option de type définie sur **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="932b5-p102">A **Connection** is a non-persistent object that represents a connection to a remote database. The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>


> [!NOTE]
> <P><span data-ttu-id="932b5-p103">[!REMARQUE] Le code écrit pour des versions antérieures de DAO peut continuer à utiliser l'objet <STRONG>Database</STRONG> pour la rétrocompatibilité, mais si les nouvelles caractéristiques d'un objet <STRONG>Connection</STRONG> sont souhaitées, vous devez réviser le code de manière à utiliser l'objet <STRONG>Connection</STRONG>. Pour vous aider avec la conversion du code, vous pouvez obtenir une référence d'objet <STRONG>Connection</STRONG> à partir d'un objet <STRONG>Database</STRONG> en lisant la propriété <A href="database-connection-property-dao.md">Connection</A> de l'objet <STRONG>Database</STRONG>. À l'inverse, vous pouvez obtenir une référence d'objet <STRONG>Database</STRONG> à partir de la propriété <STRONG>Database</STRONG> de l'objet <STRONG>Connection</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="932b5-p103">Code written for earlier versions of DAO can continue to use the <STRONG>Database</STRONG> object for backward compatibility, but if the new features of a <STRONG>Connection</STRONG> are desired, you should revise code to use the <STRONG>Connection</STRONG> object. To help with code conversion, you can obtain a <STRONG>Connection</STRONG> object reference from a <STRONG>Database</STRONG> by reading the <A href="database-connection-property-dao.md">Connection</A> property of the <STRONG>Database</STRONG> object. Conversely, you can obtain a <STRONG>Database</STRONG> object reference from the <STRONG>Connection</STRONG> object's <STRONG>Database</STRONG> property.</span></span></P>



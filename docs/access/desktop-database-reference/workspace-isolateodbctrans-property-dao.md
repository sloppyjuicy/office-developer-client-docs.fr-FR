---
title: Propriété Workspace.IsolateODBCTrans (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2e0649fd29a2bed21a894334b34cfe64bc9b3563
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930041"
---
# <a name="workspaceisolateodbctrans-property-dao"></a><span data-ttu-id="81ab9-102">Propriété Workspace.IsolateODBCTrans (DAO)</span><span class="sxs-lookup"><span data-stu-id="81ab9-102">Workspace.IsolateODBCTrans property (DAO)</span></span>


<span data-ttu-id="81ab9-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81ab9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81ab9-104">Définit ou renvoie une valeur qui indique si plusieurs transactions impliquant la même source de données ODBC connectée au moteur de base de données Microsoft Access sont isolées (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="81ab9-104">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="81ab9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81ab9-105">Syntax</span></span>

<span data-ttu-id="81ab9-106">*expression* . IsolateODBCTrans</span><span class="sxs-lookup"><span data-stu-id="81ab9-106">*expression* .IsolateODBCTrans</span></span>

<span data-ttu-id="81ab9-107">*expression* Variable qui représente un objet **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="81ab9-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="81ab9-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="81ab9-108">Remarks</span></span>

<span data-ttu-id="81ab9-p101">Dans certaines situations, il est nécessaire d'avoir plusieurs transactions simultanées en cours sur la même connexion ODBC. Pour ce faire, vous devez ouvrir un objet **Workspace** séparé pour chaque transaction. Bien que chaque objet **Workspace** peut avoir sa propre connexion ODBC à la base de données, ceci ralentit les performances du système. Éant donné que l'isolation des transactions est souvent inutile, les connexions ODBC à partir de plusieurs objets **Workspace** ouverts par le même utilisateur sont partagées par défaut.</span><span class="sxs-lookup"><span data-stu-id="81ab9-p101">In some situations, you need to have multiple simultaneous transactions pending on the same ODBC connection. To do this, you need to open a separate **Workspace** for each transaction. Although each **Workspace** can have its own ODBC connection to the database, this slows system performance. Because transaction isolation isn't usually required, ODBC connections from multiple **Workspace** objects opened by the same user are shared by default.</span></span>

<span data-ttu-id="81ab9-p102">Certains serveurs ODBC, comme Microsoft SQL Server, n'autorisent pas les transactions simultanées sur une connexion unique. Si vous avez besoin de plusieurs transactions simultanées en cours sur une telle base de données, définissez la propriété **IsolateODBCTrans** sur **True** pour chaque objet **Workspace** dès que vous l'ouvrez. Ce faisant, vous forcez l'ouverture d'une connexion ODBC séparée pour chaque objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="81ab9-p102">Some ODBC servers, such as Microsoft SQL Server, don't allow simultaneous transactions on a single connection. If you need to have more than one transaction at a time pending against such a database, set the **IsolateODBCTrans** property to **True** on each **Workspace** as soon as you open it. This forces a separate ODBC connection for each **Workspace**.</span></span>


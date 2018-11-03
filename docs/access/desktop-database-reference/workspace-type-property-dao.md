---
title: Propriété Workspace.Type (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c715da6ec535d90397b49e47be6ca76a72e5685
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926772"
---
# <a name="workspacetype-property-dao"></a><span data-ttu-id="6e3e2-102">Propriété Workspace.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="6e3e2-102">Workspace.Type property (DAO)</span></span>


<span data-ttu-id="6e3e2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e3e2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e3e2-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6e3e2-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3e2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e3e2-106">Syntax</span></span>

<span data-ttu-id="6e3e2-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="6e3e2-107">*expression* .Type</span></span>

<span data-ttu-id="6e3e2-108">*expression* Variable qui représente un objet **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="6e3e2-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e3e2-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e3e2-109">Remarks</span></span>

<span data-ttu-id="6e3e2-110">Pour un objet **Workspace**, les valeurs des paramètres et de retour possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="6e3e2-110">For a **Workspace** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e3e2-111">Constante</span><span class="sxs-lookup"><span data-stu-id="6e3e2-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="6e3e2-112">Type d'espace de travail</span><span class="sxs-lookup"><span data-stu-id="6e3e2-112">Workspace type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e3e2-113"><strong>dbUseJet</strong></span><span class="sxs-lookup"><span data-stu-id="6e3e2-113"><strong>dbUseJet</strong></span></span></p></td>
<td><p><span data-ttu-id="6e3e2-114">L'<strong>espace de travail</strong> est connecté au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6e3e2-114">The <strong>Workspace</strong> is connected to the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e3e2-115"><strong>dbUseODBC</strong></span><span class="sxs-lookup"><span data-stu-id="6e3e2-115"><strong>dbUseODBC</strong></span></span></p></td>
<td><p><span data-ttu-id="6e3e2-116">L'<strong>espace de travail</strong> est connecté à une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="6e3e2-116">The <strong>Workspace</strong> is connected to an ODBC data source.</span></span></p></td>
</tr>
</tbody>
</table>


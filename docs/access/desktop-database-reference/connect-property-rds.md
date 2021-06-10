---
title: Connecter propriété (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295981"
---
# <a name="connect-property-rds"></a><span data-ttu-id="69ed8-102">Connecter propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="69ed8-102">Connect property (RDS)</span></span>

<span data-ttu-id="69ed8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69ed8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69ed8-104">Indique le nom de la base de données dans laquelle les opérations de requête et de mise à jour sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="69ed8-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="69ed8-105">Vous pouvez définir la propriété **Connect** au moment du design dans les balises OBJECT de l’objet [RDS.DataControl](datacontrol-object-rds.md) ou au moment de l’exécution dans le code de script (par exemple, VBScript).</span><span class="sxs-lookup"><span data-stu-id="69ed8-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="69ed8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69ed8-106">Syntax</span></span>

<span data-ttu-id="69ed8-107">Moment de la conception \< : PARAM NAME="Connecter » VALUE="ConnectionString »\></span><span class="sxs-lookup"><span data-stu-id="69ed8-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="69ed8-108">Durée d’application : DataControl. Connecter = « ConnectionString »</span><span class="sxs-lookup"><span data-stu-id="69ed8-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="69ed8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69ed8-109">Parameters</span></span>

|<span data-ttu-id="69ed8-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="69ed8-110">Parameter</span></span>|<span data-ttu-id="69ed8-111">Description</span><span class="sxs-lookup"><span data-stu-id="69ed8-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="69ed8-112">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="69ed8-112">*ConnectionString*</span></span> |<span data-ttu-id="69ed8-p101">Chaîne de connexion valide. Pour plus d'informations d'ordre général sur les chaînes de connexion, reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md) ou à la documentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="69ed8-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span><br/><br/><span data-ttu-id="69ed8-115">**REMARQUE**: spécifier MS Remote comme fournisseur pour **rdS. DataControl** créerait un scénario à quatre niveaux.</span><span class="sxs-lookup"><span data-stu-id="69ed8-115">**NOTE**: Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario.</span></span> <span data-ttu-id="69ed8-116">Les scénarios comptant plus de trois niveaux n'ont pas été testés et sont normalement inutiles.</span><span class="sxs-lookup"><span data-stu-id="69ed8-116">Scenarios greater than three tiers have not been tested and should not be needed.</span></span>|
|<span data-ttu-id="69ed8-117">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="69ed8-117">*DataControl*</span></span> |<span data-ttu-id="69ed8-118">Une variable objet qui représente un objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="69ed8-118">An object variable that represents an **RDS.DataControl** object.</span></span>|


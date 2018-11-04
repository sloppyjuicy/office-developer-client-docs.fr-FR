---
title: Connect, propriété (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b0d0969d9cbcf972a1b57faf27bbea1dfd960d5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949417"
---
# <a name="connect-property-rds"></a><span data-ttu-id="928b4-102">Connect, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="928b4-102">Connect property (RDS)</span></span>

<span data-ttu-id="928b4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="928b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="928b4-104">Indique le nom de la base de données dans laquelle les opérations de requête et de mise à jour sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="928b4-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="928b4-105">Vous pouvez définir la propriété **Connect** au moment du design dans les balises OBJECT de l'objet [RDS.DataControl](datacontrol-object-rds.md) ou au moment de l'exécution dans le code de script (par exemple, VBScript).</span><span class="sxs-lookup"><span data-stu-id="928b4-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="928b4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="928b4-106">Syntax</span></span>

<span data-ttu-id="928b4-107">Au moment du design : \<PARAM NAME = « Connexion », valeur = « ConnectionString »\></span><span class="sxs-lookup"><span data-stu-id="928b4-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="928b4-108">Temps d’exécution : DataControl.Connect = « ConnectionString »</span><span class="sxs-lookup"><span data-stu-id="928b4-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="928b4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="928b4-109">Parameters</span></span>

|<span data-ttu-id="928b4-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="928b4-110">Parameter</span></span>|<span data-ttu-id="928b4-111">Description</span><span class="sxs-lookup"><span data-stu-id="928b4-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="928b4-112">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="928b4-112">*ConnectionString*</span></span> |<span data-ttu-id="928b4-p101">Chaîne de connexion valide. Pour plus d'informations d'ordre général sur les chaînes de connexion, reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md) ou à la documentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="928b4-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span><br/><br/><span data-ttu-id="928b4-115">**Remarque**: spécification MS Remote comme fournisseur pour le **RDS. DataControl** crée un scénario à quatre niveaux.</span><span class="sxs-lookup"><span data-stu-id="928b4-115">**NOTE**: Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario.</span></span> <span data-ttu-id="928b4-116">Les scénarios comptant plus de trois niveaux n'ont pas été testés et sont normalement inutiles.</span><span class="sxs-lookup"><span data-stu-id="928b4-116">Scenarios greater than three tiers have not been tested and should not be needed.</span></span>|
|<span data-ttu-id="928b4-117">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="928b4-117">*DataControl*</span></span> |<span data-ttu-id="928b4-118">Une variable objet qui représente un objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="928b4-118">An object variable that represents an **RDS.DataControl** object.</span></span>|


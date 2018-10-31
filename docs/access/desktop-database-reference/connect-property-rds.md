---
title: Connect, propriété (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 191ef13d4d3c73bfbee50d72720d7e450376dd23
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862918"
---
# <a name="connect-property-rds"></a><span data-ttu-id="e8b4c-102">Connect, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="e8b4c-102">Connect Property (RDS)</span></span>


<span data-ttu-id="e8b4c-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8b4c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8b4c-104">Indique le nom de la base de données dans laquelle les opérations de requête et de mise à jour sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="e8b4c-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="e8b4c-105">Vous pouvez définir la propriété **Connect** au moment du design dans les balises OBJECT de l'objet [RDS.DataControl](datacontrol-object-rds.md) ou au moment de l'exécution dans le code de script (par exemple, VBScript).</span><span class="sxs-lookup"><span data-stu-id="e8b4c-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b4c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8b4c-106">Syntax</span></span>

<span data-ttu-id="e8b4c-107">Au moment du design : \<PARAM NAME = « Connexion », valeur = « ConnectionString »\></span><span class="sxs-lookup"><span data-stu-id="e8b4c-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="e8b4c-108">Temps d’exécution : DataControl.Connect = « ConnectionString »</span><span class="sxs-lookup"><span data-stu-id="e8b4c-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="e8b4c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8b4c-109">Parameters</span></span>

- <span data-ttu-id="e8b4c-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="e8b4c-110">*ConnectionString*</span></span>

  - <span data-ttu-id="e8b4c-p101">Chaîne de connexion valide. Pour plus d'informations d'ordre général sur les chaînes de connexion, reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md) ou à la documentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e8b4c-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e8b4c-p102">[!REMARQUE] Si vous spécifiez MS Remote comme fournisseur de l'objet **RDS.DataControl**, un scénario à quatre niveaux est créé. Les scénarios comptant plus de trois niveaux n'ont pas été testés et sont normalement inutiles.</span><span class="sxs-lookup"><span data-stu-id="e8b4c-p102">Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario. Scenarios greater than three tiers have not been tested and should not be needed.</span></span>

- <span data-ttu-id="e8b4c-115">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="e8b4c-115">*DataControl*</span></span>

  - <span data-ttu-id="e8b4c-116">Une variable objet qui représente un objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="e8b4c-116">An object variable that represents an **RDS.DataControl** object.</span></span>


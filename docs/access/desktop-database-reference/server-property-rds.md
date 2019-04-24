---
title: Server, propriété (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f35910591d86e0e5a2b92d680be3c5f64504088
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308686"
---
# <a name="server-property-rds"></a><span data-ttu-id="b05c1-102">Server, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="b05c1-102">Server property (RDS)</span></span>

<span data-ttu-id="b05c1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b05c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b05c1-104">Indique le nom de l'IIS (Internet Information Services) et du protocole de communication.</span><span class="sxs-lookup"><span data-stu-id="b05c1-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="b05c1-105">Vous pouvez définir la propriété **Server** à la conception dans les balises OBJECT de l’objet [RDS.DataControl](datacontrol-object-rds.md) ou à l’exécution dans le code de script.</span><span class="sxs-lookup"><span data-stu-id="b05c1-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b05c1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b05c1-106">Syntax</span></span>

|<span data-ttu-id="b05c1-107">Protocole</span><span class="sxs-lookup"><span data-stu-id="b05c1-107">Protocol</span></span>|<span data-ttu-id="b05c1-108">Syntaxe à la conception</span><span class="sxs-lookup"><span data-stu-id="b05c1-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="b05c1-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="b05c1-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="b05c1-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b05c1-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="b05c1-111">APPELER</span><span class="sxs-lookup"><span data-stu-id="b05c1-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="b05c1-112">In-process</span><span class="sxs-lookup"><span data-stu-id="b05c1-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="b05c1-113">Protocole</span><span class="sxs-lookup"><span data-stu-id="b05c1-113">Protocol</span></span>|<span data-ttu-id="b05c1-114">Syntaxe à l'exécution</span><span class="sxs-lookup"><span data-stu-id="b05c1-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="b05c1-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="b05c1-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="b05c1-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b05c1-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="b05c1-117">APPELER</span><span class="sxs-lookup"><span data-stu-id="b05c1-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="b05c1-118">In-process</span><span class="sxs-lookup"><span data-stu-id="b05c1-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="b05c1-119">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b05c1-119">Parameters</span></span>

|<span data-ttu-id="b05c1-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="b05c1-120">Parameter</span></span>|<span data-ttu-id="b05c1-121">Description</span><span class="sxs-lookup"><span data-stu-id="b05c1-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b05c1-122">*awebsrvr* ou *computername*</span><span class="sxs-lookup"><span data-stu-id="b05c1-122">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="b05c1-123">Une valeur **String** qui contient un chemin d'accès Internet ou intranet, un nom d'ordinateur (si le serveur se trouve sur un ordinateur distant) ou une chaîne vide si le serveur se trouve sur l'ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b05c1-123">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>|
|<span data-ttu-id="b05c1-124">*port*</span><span class="sxs-lookup"><span data-stu-id="b05c1-124">*port*</span></span> |<span data-ttu-id="b05c1-p101">Facultatif. Un port utilisé pour se connecter à un serveur IIS. Le numéro du port est défini dans Internet Explorer (dans le menu **Outils**, cliquez sur **Options Internet** et sélectionnez l'onglet **Connexion** ) ou dans IIS.</span><span class="sxs-lookup"><span data-stu-id="b05c1-p101">Optional. A port that is used to connect to an IIS server. The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>|
|<span data-ttu-id="b05c1-128">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b05c1-128">*DataControl*</span></span> |<span data-ttu-id="b05c1-129">Une variable objet qui représente un objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="b05c1-129">An object variable that represents an **RDS.DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b05c1-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="b05c1-130">Remarks</span></span>

<span data-ttu-id="b05c1-131">Le serveur est l'endroit où la requête **RDS.DataControl** (une demande ou une mise à jour) est traitée.</span><span class="sxs-lookup"><span data-stu-id="b05c1-131">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="b05c1-132">Par défaut, toutes les requêtes sont traitées par l'objet [RDSServer.DataFactory](datafactory-object-rdsserver.md), le composant [MSDFMAP.Handler](datafactory-customization.md) et le fichier [MSDFMAP.INI](understanding-the-customization-file.md) sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="b05c1-132">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="b05c1-133">Souvenez-vous, lorsque vous changez de serveur, de comparer les paramètres des anciens et des nouveaux fichiers **MSDFMAP.INI**.</span><span class="sxs-lookup"><span data-stu-id="b05c1-133">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="b05c1-134">S'ils ne sont pas compatibles, les requêtes qui aboutissent sur un serveur peuvent générer des erreurs sur un autre.</span><span class="sxs-lookup"><span data-stu-id="b05c1-134">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="b05c1-135">Si la valeur de la propriété Server est « », ces objets seront utilisés sur la machine locale.</span><span class="sxs-lookup"><span data-stu-id="b05c1-135">If the Server property is set to "", these objects will be used on the local machine.</span></span>


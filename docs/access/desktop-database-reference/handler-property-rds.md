---
title: Propriété Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292068"
---
# <a name="handler-property-rds"></a><span data-ttu-id="9cea6-102">Propriété Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="9cea6-102">Handler property (RDS)</span></span>

<span data-ttu-id="9cea6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9cea6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9cea6-104">Indique le nom d’un programme de personnalisation coté serveur (gestionnaire) qui étend la fonctionnalité de [RDSServer.DataFactory](datafactory-object-rdsserver.md) et tous les paramètres utilisés par le *gestionnaire (handler)*.</span><span class="sxs-lookup"><span data-stu-id="9cea6-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cea6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9cea6-105">Syntax</span></span>

<span data-ttu-id="9cea6-106">*DataControl*. Handler = *String*</span><span class="sxs-lookup"><span data-stu-id="9cea6-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="9cea6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9cea6-107">Parameters</span></span>

|<span data-ttu-id="9cea6-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="9cea6-108">Parameter</span></span>|<span data-ttu-id="9cea6-109">Description</span><span class="sxs-lookup"><span data-stu-id="9cea6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9cea6-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="9cea6-110">*DataControl*</span></span> |<span data-ttu-id="9cea6-111">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="9cea6-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="9cea6-112">*String*</span><span class="sxs-lookup"><span data-stu-id="9cea6-112">*String*</span></span> |<span data-ttu-id="9cea6-113">Valeur **de** chaîne qui contient le nom du handler et tous les paramètres, séparés par des virgules (par exemple, « handlerName,parm1,parm2,...,parm *N*».</span><span class="sxs-lookup"><span data-stu-id="9cea6-113">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="9cea6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9cea6-114">Remarks</span></span>

<span data-ttu-id="9cea6-115">Cette propriété prend en charge la personnalisation, fonctionnalité pour laquelle il faut donner à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="9cea6-115">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="9cea6-p101">Les noms du gestionnaire et de ses paramètres, le cas échéant, sont séparés par des virgules (« , »). Le comportement n'est pas garanti si un point-virgule (« ; ») apparaît dans la valeur *String*. Vous pouvez écrire votre propre gestionnaire à condition qu'il prenne en charge l'interface **IDataFactoryHandler**.</span><span class="sxs-lookup"><span data-stu-id="9cea6-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="9cea6-p102">Le gestionnaire par défaut s'appelle **MSDFMAP.Handler**, son paramètre par défaut est un fichier de personnalisation appelé **MSDFMAP.INI**. Utilisez cette propriété pour appeler les autres fichiers de personnalisation créés par votre administrateur serveur.</span><span class="sxs-lookup"><span data-stu-id="9cea6-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="9cea6-121">L’alternative à la définition de la propriété **Handler** consiste à spécifier un handler et des paramètres dans la [propriété ConnectionString](connectionstring-property-ado.md) ; autrement dit, « \**Handler=\*\*\*handlerName,parm1,parm2,...;*».</span><span class="sxs-lookup"><span data-stu-id="9cea6-121">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>


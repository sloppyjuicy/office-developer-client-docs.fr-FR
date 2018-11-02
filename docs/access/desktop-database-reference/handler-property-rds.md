---
title: Handler, propriété (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bb9444091611fbd051da9fa649b5d3efdb92ee6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923580"
---
# <a name="handler-property-rds"></a><span data-ttu-id="21d8f-102">Handler, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="21d8f-102">Handler property (RDS)</span></span>


<span data-ttu-id="21d8f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21d8f-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="21d8f-104">Indique le nom d’un programme de personnalisation coté serveur (gestionnaire) qui étend la fonctionnalité de [RDSServer.DataFactory](datafactory-object-rdsserver.md) et tous les paramètres utilisés par le *gestionnaire (handler)*.</span><span class="sxs-lookup"><span data-stu-id="21d8f-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d8f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21d8f-105">Syntax</span></span>

<span data-ttu-id="21d8f-106">*DataControl*. Gestionnaire = *chaîne*</span><span class="sxs-lookup"><span data-stu-id="21d8f-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="21d8f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21d8f-107">Parameters</span></span>

  - <span data-ttu-id="21d8f-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="21d8f-108">*DataControl*</span></span>

  - <span data-ttu-id="21d8f-109">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="21d8f-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="21d8f-110">*String*</span><span class="sxs-lookup"><span data-stu-id="21d8f-110">*String*</span></span>

  - <span data-ttu-id="21d8f-111">Une valeur de **type String** qui contient le nom du gestionnaire et des paramètres, séparés par des virgules (par exemple, « handlerName, parm1, parm2,..., parm *N*»).</span><span class="sxs-lookup"><span data-stu-id="21d8f-111">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>

## <a name="remarks"></a><span data-ttu-id="21d8f-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="21d8f-112">Remarks</span></span>

<span data-ttu-id="21d8f-113">Cette propriété prend en charge la personnalisation, fonctionnalité pour laquelle il faut donner à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="21d8f-113">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="21d8f-p101">Les noms du gestionnaire et de ses paramètres, le cas échéant, sont séparés par des virgules (« , »). Le comportement n'est pas garanti si un point-virgule (« ; ») apparaît dans la valeur *String*. Vous pouvez écrire votre propre gestionnaire à condition qu'il prenne en charge l'interface **IDataFactoryHandler**.</span><span class="sxs-lookup"><span data-stu-id="21d8f-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="21d8f-p102">Le gestionnaire par défaut s'appelle **MSDFMAP.Handler**, son paramètre par défaut est un fichier de personnalisation appelé **MSDFMAP.INI**. Utilisez cette propriété pour appeler les autres fichiers de personnalisation créés par votre administrateur serveur.</span><span class="sxs-lookup"><span data-stu-id="21d8f-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="21d8f-119">Définir la propriété **Handler** consiste à spécifier un gestionnaire et des paramètres dans la propriété [ConnectionString](connectionstring-property-ado.md) . Autrement dit, « \**Gestionnaire = \*\*\* handlerName, parm1, parm2,... ;*».</span><span class="sxs-lookup"><span data-stu-id="21d8f-119">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>


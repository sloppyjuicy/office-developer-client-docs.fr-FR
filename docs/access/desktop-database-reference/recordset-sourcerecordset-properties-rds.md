---
title: Recordset, SourceRecordset, propriétés (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f83ab385b1fab511ab71ea9ff3456fe466efa17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307587"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="467f1-102">Recordset, SourceRecordset, propriétés (RDS)</span><span class="sxs-lookup"><span data-stu-id="467f1-102">Recordset, SourceRecordset properties (RDS)</span></span>

<span data-ttu-id="467f1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="467f1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="467f1-104">Indique l’objet **Recordset** retourné d’un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="467f1-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="467f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="467f1-105">Syntax</span></span>

<span data-ttu-id="467f1-106">*DataControl*. SourceRecordset = *Jeu d’enregistrements*</span><span class="sxs-lookup"><span data-stu-id="467f1-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="467f1-107">*Recordset*  =  *DataControl*. Recordset</span><span class="sxs-lookup"><span data-stu-id="467f1-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="467f1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="467f1-108">Parameters</span></span>

|<span data-ttu-id="467f1-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="467f1-109">Parameter</span></span>|<span data-ttu-id="467f1-110">Description</span><span class="sxs-lookup"><span data-stu-id="467f1-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="467f1-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="467f1-111">*DataControl*</span></span> |<span data-ttu-id="467f1-112">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="467f1-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="467f1-113">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="467f1-113">*Recordset*</span></span> |<span data-ttu-id="467f1-114">Variable objet représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="467f1-114">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="467f1-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="467f1-115">Remarks</span></span>

<span data-ttu-id="467f1-116">Vous pouvez donner comme valeur à la propriété **SourceRecordset** un [Recordset](recordset-object-ado.md) renvoyé par un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="467f1-116">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="467f1-p101">Ces propriétés permettent à une application de gérer le processus de liaison au moyen d'un processus personnalisé. Elles reçoivent un ensemble de lignes inséré dans un **Recordset**, pour que vous puissiez agir directement sur le **Recordset** (définition de propriétés ou itérations dans le **Recordset** ).</span><span class="sxs-lookup"><span data-stu-id="467f1-p101">These properties allow an application to handle the binding process by means of a custom process. They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="467f1-119">Vous pouvez définir la propriété **SourceRecordset** ou lire la propriété **Recordset** en mode exécution dans le code de script.</span><span class="sxs-lookup"><span data-stu-id="467f1-119">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="467f1-120">**SourceRecordset** est une propriété en écriture seule, contrairement à la propriété **Recordset** qui est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="467f1-120">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>


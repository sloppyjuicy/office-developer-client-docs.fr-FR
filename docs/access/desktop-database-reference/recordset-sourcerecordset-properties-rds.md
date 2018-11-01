---
title: Recordset, SourceRecordset, propriétés (RDS)
TOCTitle: Recordset, SourceRecordset Properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 08fe0f569b36fe0b3403cb564dc53eadf2edff8c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887179"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="03ee7-102">Recordset, SourceRecordset, propriétés (RDS)</span><span class="sxs-lookup"><span data-stu-id="03ee7-102">Recordset, SourceRecordset Properties (RDS)</span></span>


<span data-ttu-id="03ee7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03ee7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03ee7-104">Indique l'objet **Recordset** retourné d'un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="03ee7-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ee7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03ee7-105">Syntax</span></span>

<span data-ttu-id="03ee7-106">*DataControl*. SourceRecordset = le *jeu d’enregistrements*</span><span class="sxs-lookup"><span data-stu-id="03ee7-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="03ee7-107">*Jeu d’enregistrements* = *DataControl*. Jeu d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="03ee7-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="03ee7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03ee7-108">Parameters</span></span>

  - <span data-ttu-id="03ee7-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="03ee7-109">*DataControl*</span></span>

  - <span data-ttu-id="03ee7-110">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="03ee7-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="03ee7-111">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="03ee7-111">*Recordset*</span></span>

  - <span data-ttu-id="03ee7-112">Variable objet représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="03ee7-112">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="03ee7-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="03ee7-113">Remarks</span></span>

<span data-ttu-id="03ee7-114">Vous pouvez donner comme valeur à la propriété **SourceRecordset** un [Recordset](recordset-object-ado.md) renvoyé par un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="03ee7-114">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="03ee7-p101">Ces propriétés permettent à une application de gérer le processus de liaison au moyen d'un processus personnalisé. Elles reçoivent un ensemble de lignes inséré dans un **Recordset**, pour que vous puissiez agir directement sur le **Recordset** (définition de propriétés ou itérations dans le **Recordset** ).</span><span class="sxs-lookup"><span data-stu-id="03ee7-p101">These properties allow an application to handle the binding process by means of a custom process. They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="03ee7-117">Vous pouvez définir la propriété **SourceRecordset** ou lire la propriété **Recordset** en mode exécution dans le code de script.</span><span class="sxs-lookup"><span data-stu-id="03ee7-117">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="03ee7-118">**SourceRecordset** est une propriété en écriture seule, contrairement à la propriété **Recordset** qui est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="03ee7-118">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>


---
title: Propriétés dynamiques du jeu d'enregistrements au format XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48714b9178e99cfd4ccf7738f3ad4a342572fdfa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884260"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="657d7-102">Propriétés dynamiques du jeu d'enregistrements au format XML</span><span class="sxs-lookup"><span data-stu-id="657d7-102">Recordset Dynamic Properties in XML</span></span>


<span data-ttu-id="657d7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="657d7-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="657d7-104">Propriétés dynamiques du jeu d'enregistrements au format XML</span><span class="sxs-lookup"><span data-stu-id="657d7-104">Recordset Dynamic Properties in XML</span></span>

<span data-ttu-id="657d7-105">Les propriétés **Recordset** spécifiques au fournisseur (du moteur du curseur client) suivantes sont actuellement conservées au format XML :</span><span class="sxs-lookup"><span data-stu-id="657d7-105">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

  - <span data-ttu-id="657d7-106">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="657d7-106">**Update Resync**</span></span>

  - <span data-ttu-id="657d7-107">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="657d7-107">**Unique Table**</span></span>

  - <span data-ttu-id="657d7-108">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="657d7-108">**Unique Schema**</span></span>

  - <span data-ttu-id="657d7-109">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="657d7-109">**Unique Catalog**</span></span>

  - <span data-ttu-id="657d7-110">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="657d7-110">**Resync Command**</span></span>

  - <span data-ttu-id="657d7-111">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="657d7-111">**IRowsetChange**</span></span>

  - <span data-ttu-id="657d7-112">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="657d7-112">**IRowsetUpdate**</span></span>

  - <span data-ttu-id="657d7-113">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="657d7-113">**CommandTimeout**</span></span>

  - <span data-ttu-id="657d7-114">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="657d7-114">**BatchSize**</span></span>

  - <span data-ttu-id="657d7-115">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="657d7-115">**UpdateCriteria**</span></span>

  - <span data-ttu-id="657d7-116">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="657d7-116">**Reshape Name**</span></span>

  - <span data-ttu-id="657d7-117">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="657d7-117">**AutoRecalc**</span></span>

<span data-ttu-id="657d7-p101">Ces propriétés sont enregistrées dans la section de schéma en tant qu'attributs de la définition d'élément du **jeu d'enregistrements** en cours de persistance. Ces attributs sont définis dans l'espace de noms du schéma du jeu de lignes et doivent avoir le préfixe « rs: ».</span><span class="sxs-lookup"><span data-stu-id="657d7-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>


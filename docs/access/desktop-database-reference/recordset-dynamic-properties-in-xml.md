---
title: Propriétés dynamiques du recordset au format XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36069ec0e8e9020bc70ef1ea72ce25f4461c6487
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946957"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="41a8c-102">Propriétés dynamiques du recordset au format XML</span><span class="sxs-lookup"><span data-stu-id="41a8c-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="41a8c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41a8c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41a8c-104">Les propriétés **Recordset** spécifiques au fournisseur (du moteur du curseur client) suivantes sont actuellement conservées au format XML :</span><span class="sxs-lookup"><span data-stu-id="41a8c-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="41a8c-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="41a8c-105">**AutoRecalc**</span></span>
- <span data-ttu-id="41a8c-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="41a8c-106">**BatchSize**</span></span>
- <span data-ttu-id="41a8c-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="41a8c-107">**CommandTimeout**</span></span>
- <span data-ttu-id="41a8c-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="41a8c-108">**IRowsetChange**</span></span>
- <span data-ttu-id="41a8c-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="41a8c-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="41a8c-110">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="41a8c-110">**Reshape Name**</span></span>
- <span data-ttu-id="41a8c-111">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="41a8c-111">**Resync Command**</span></span>
- <span data-ttu-id="41a8c-112">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="41a8c-112">**Unique Catalog**</span></span>
- <span data-ttu-id="41a8c-113">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="41a8c-113">**Unique Schema**</span></span>
- <span data-ttu-id="41a8c-114">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="41a8c-114">**Unique Table**</span></span>
- <span data-ttu-id="41a8c-115">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="41a8c-115">**Update Resync**</span></span>
- <span data-ttu-id="41a8c-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="41a8c-116">**UpdateCriteria**</span></span>


<span data-ttu-id="41a8c-p101">Ces propriétés sont enregistrées dans la section de schéma en tant qu'attributs de la définition d'élément du **jeu d'enregistrements** en cours de persistance. Ces attributs sont définis dans l'espace de noms du schéma du jeu de lignes et doivent avoir le préfixe « rs: ».</span><span class="sxs-lookup"><span data-stu-id="41a8c-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="41a8c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41a8c-119">See also</span></span>

- [<span data-ttu-id="41a8c-120">Propriétés dynamiques ADO</span><span class="sxs-lookup"><span data-stu-id="41a8c-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)
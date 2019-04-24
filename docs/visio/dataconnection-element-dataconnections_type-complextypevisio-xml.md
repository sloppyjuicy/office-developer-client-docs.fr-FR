---
title: DataConnection, élément (DataConnections_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Extrait la communication entre un ou plusieurs éléments DataRecordset et une source de données non XML.
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344624"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="06b09-103">DataConnection, élément (DataConnections_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="06b09-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="06b09-104">Extrait la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML.</span><span class="sxs-lookup"><span data-stu-id="06b09-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="06b09-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="06b09-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06b09-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="06b09-106">**Element type**</span></span> <br/> |[<span data-ttu-id="06b09-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="06b09-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="06b09-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="06b09-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="06b09-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="06b09-109">**Schema file**</span></span> <br/> |<span data-ttu-id="06b09-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="06b09-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="06b09-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="06b09-111">**Document parts**</span></span> <br/> |<span data-ttu-id="06b09-112">Connections. Xml</span><span class="sxs-lookup"><span data-stu-id="06b09-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="06b09-113">Définition</span><span class="sxs-lookup"><span data-stu-id="06b09-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="06b09-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="06b09-114">Elements and attributes</span></span>

<span data-ttu-id="06b09-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="06b09-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="06b09-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="06b09-116">Parent elements</span></span>

|<span data-ttu-id="06b09-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="06b09-117">**Element**</span></span>|<span data-ttu-id="06b09-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="06b09-118">**Type**</span></span>|<span data-ttu-id="06b09-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="06b09-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="06b09-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="06b09-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="06b09-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="06b09-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="06b09-122">Contient les éléments **DataConnection** pour le document.</span><span class="sxs-lookup"><span data-stu-id="06b09-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="06b09-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="06b09-123">Child elements</span></span>

<span data-ttu-id="06b09-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="06b09-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06b09-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="06b09-125">Attributes</span></span>

|<span data-ttu-id="06b09-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="06b09-126">**Attribute**</span></span>|<span data-ttu-id="06b09-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="06b09-127">**Type**</span></span>|<span data-ttu-id="06b09-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="06b09-128">**Required**</span></span>|<span data-ttu-id="06b09-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="06b09-129">**Description**</span></span>|<span data-ttu-id="06b09-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="06b09-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="06b09-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="06b09-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="06b09-132">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="06b09-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="06b09-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="06b09-133">optional</span></span>  <br/> |<span data-ttu-id="06b09-134">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="06b09-134">The default value is false.</span></span> <span data-ttu-id="06b09-135">Voir la section Remarques pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="06b09-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="06b09-136">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="06b09-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="06b09-137">Command</span><span class="sxs-lookup"><span data-stu-id="06b09-137">Command</span></span>  <br/> |<span data-ttu-id="06b09-138">xsd: String</span><span class="sxs-lookup"><span data-stu-id="06b09-138">xsd:string</span></span>  <br/> |<span data-ttu-id="06b09-139">facultatif</span><span class="sxs-lookup"><span data-stu-id="06b09-139">optional</span></span>  <br/> |<span data-ttu-id="06b09-140">Chaîne de commande utilisée pour interroger la source de données.</span><span class="sxs-lookup"><span data-stu-id="06b09-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="06b09-141">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="06b09-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="06b09-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="06b09-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="06b09-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="06b09-143">xsd:string</span></span>  <br/> |<span data-ttu-id="06b09-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="06b09-144">optional</span></span>  <br/> |<span data-ttu-id="06b09-145">Chaîne de connexion qui définit les paramètres nécessaires pour se connecter à une source de données.</span><span class="sxs-lookup"><span data-stu-id="06b09-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="06b09-146">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="06b09-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="06b09-147">FileName</span><span class="sxs-lookup"><span data-stu-id="06b09-147">FileName</span></span>  <br/> |<span data-ttu-id="06b09-148">xsd: String</span><span class="sxs-lookup"><span data-stu-id="06b09-148">xsd:string</span></span>  <br/> |<span data-ttu-id="06b09-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="06b09-149">required</span></span>  <br/> |<span data-ttu-id="06b09-150">Nom du fichier de connexion.</span><span class="sxs-lookup"><span data-stu-id="06b09-150">The name of the connection file.</span></span> <span data-ttu-id="06b09-151">Voir la section Remarques pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="06b09-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="06b09-152">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="06b09-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="06b09-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="06b09-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="06b09-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="06b09-154">xsd:string</span></span>  <br/> |<span data-ttu-id="06b09-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="06b09-155">optional</span></span>  <br/> |<span data-ttu-id="06b09-156">Un nom fourni par l'utilisateur pour la connexion de données.</span><span class="sxs-lookup"><span data-stu-id="06b09-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="06b09-157">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="06b09-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="06b09-158">ID</span><span class="sxs-lookup"><span data-stu-id="06b09-158">ID</span></span>  <br/> |<span data-ttu-id="06b09-159">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="06b09-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="06b09-160">obligatoire</span><span class="sxs-lookup"><span data-stu-id="06b09-160">required</span></span>  <br/> |<span data-ttu-id="06b09-161">ID attribué par Visio pour une connexion donnée, unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="06b09-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="06b09-162">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="06b09-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="06b09-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="06b09-163">Timeout</span></span>  <br/> |<span data-ttu-id="06b09-164">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="06b09-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="06b09-165">facultatif</span><span class="sxs-lookup"><span data-stu-id="06b09-165">optional</span></span>  <br/> |<span data-ttu-id="06b09-166">Temps d'attente en minutes lors d'une tentative d'établissement d'une connexion avant la fin de la tentative.</span><span class="sxs-lookup"><span data-stu-id="06b09-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="06b09-167">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="06b09-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


---
title: Élément DataConnection (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Extrait la communication entre un ou plusieurs éléments DataRecordset et une source de données non XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538402"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="17203-103">Élément DataConnection (DataConnections_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="17203-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="17203-104">Extrait la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML.</span><span class="sxs-lookup"><span data-stu-id="17203-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="17203-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="17203-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17203-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="17203-106">**Element type**</span></span> <br/> |[<span data-ttu-id="17203-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="17203-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="17203-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="17203-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="17203-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="17203-109">**Schema file**</span></span> <br/> |<span data-ttu-id="17203-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="17203-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="17203-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="17203-111">**Document parts**</span></span> <br/> |<span data-ttu-id="17203-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="17203-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17203-113">Définition</span><span class="sxs-lookup"><span data-stu-id="17203-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="17203-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="17203-114">Elements and attributes</span></span>

<span data-ttu-id="17203-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="17203-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="17203-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="17203-116">Parent elements</span></span>

|<span data-ttu-id="17203-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="17203-117">**Element**</span></span>|<span data-ttu-id="17203-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="17203-118">**Type**</span></span>|<span data-ttu-id="17203-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="17203-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17203-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="17203-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="17203-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="17203-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17203-122">Contient les **éléments DataConnection** du document.</span><span class="sxs-lookup"><span data-stu-id="17203-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="17203-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="17203-123">Child elements</span></span>

<span data-ttu-id="17203-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="17203-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17203-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="17203-125">Attributes</span></span>

|<span data-ttu-id="17203-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="17203-126">**Attribute**</span></span>|<span data-ttu-id="17203-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="17203-127">**Type**</span></span>|<span data-ttu-id="17203-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="17203-128">**Required**</span></span>|<span data-ttu-id="17203-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="17203-129">**Description**</span></span>|<span data-ttu-id="17203-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="17203-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="17203-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="17203-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="17203-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="17203-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="17203-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="17203-133">optional</span></span>  <br/> |<span data-ttu-id="17203-134">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="17203-134">The default value is false.</span></span> <span data-ttu-id="17203-135">Voir la section Remarques pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="17203-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="17203-136">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="17203-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="17203-137">Commande</span><span class="sxs-lookup"><span data-stu-id="17203-137">Command</span></span>  <br/> |<span data-ttu-id="17203-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="17203-138">xsd:string</span></span>  <br/> |<span data-ttu-id="17203-139">facultatif</span><span class="sxs-lookup"><span data-stu-id="17203-139">optional</span></span>  <br/> |<span data-ttu-id="17203-140">Chaîne de commande utilisée pour interroger la source de données.</span><span class="sxs-lookup"><span data-stu-id="17203-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="17203-141">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="17203-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="17203-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="17203-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="17203-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="17203-143">xsd:string</span></span>  <br/> |<span data-ttu-id="17203-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="17203-144">optional</span></span>  <br/> |<span data-ttu-id="17203-145">Chaîne de connexion qui définit les paramètres nécessaires pour se connecter à une source de données.</span><span class="sxs-lookup"><span data-stu-id="17203-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="17203-146">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="17203-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="17203-147">FileName</span><span class="sxs-lookup"><span data-stu-id="17203-147">FileName</span></span>  <br/> |<span data-ttu-id="17203-148">xsd:string</span><span class="sxs-lookup"><span data-stu-id="17203-148">xsd:string</span></span>  <br/> |<span data-ttu-id="17203-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="17203-149">required</span></span>  <br/> |<span data-ttu-id="17203-150">Nom du fichier de connexion.</span><span class="sxs-lookup"><span data-stu-id="17203-150">The name of the connection file.</span></span> <span data-ttu-id="17203-151">Voir la section Remarques pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="17203-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="17203-152">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="17203-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="17203-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="17203-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="17203-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="17203-154">xsd:string</span></span>  <br/> |<span data-ttu-id="17203-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="17203-155">optional</span></span>  <br/> |<span data-ttu-id="17203-156">Nom fourni par l’utilisateur pour la connexion de données.</span><span class="sxs-lookup"><span data-stu-id="17203-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="17203-157">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="17203-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="17203-158">ID</span><span class="sxs-lookup"><span data-stu-id="17203-158">ID</span></span>  <br/> |<span data-ttu-id="17203-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17203-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17203-160">obligatoire</span><span class="sxs-lookup"><span data-stu-id="17203-160">required</span></span>  <br/> |<span data-ttu-id="17203-161">ID attribué par le Visio pour une connexion donnée, unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="17203-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="17203-162">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="17203-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="17203-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="17203-163">Timeout</span></span>  <br/> |<span data-ttu-id="17203-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17203-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17203-165">facultatif</span><span class="sxs-lookup"><span data-stu-id="17203-165">optional</span></span>  <br/> |<span data-ttu-id="17203-166">Délai d’attente en minutes lors de la tentative d’établissement d’une connexion avant la fin de la tentative.</span><span class="sxs-lookup"><span data-stu-id="17203-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="17203-167">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="17203-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


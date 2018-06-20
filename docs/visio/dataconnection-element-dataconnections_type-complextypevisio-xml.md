---
title: DataConnection, élément (DataConnections_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Analyse la communication entre un ou plusieurs éléments DataRecordset et une source de données non XML.
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788420"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="e0285-103">DataConnection, élément (DataConnections_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="e0285-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e0285-104">Analyse la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML.</span><span class="sxs-lookup"><span data-stu-id="e0285-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e0285-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="e0285-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0285-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="e0285-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e0285-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="e0285-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e0285-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e0285-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e0285-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e0285-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e0285-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e0285-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e0285-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="e0285-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e0285-112">Connections.Xml</span><span class="sxs-lookup"><span data-stu-id="e0285-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0285-113">Définition</span><span class="sxs-lookup"><span data-stu-id="e0285-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e0285-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e0285-114">Elements and attributes</span></span>

<span data-ttu-id="e0285-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="e0285-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e0285-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e0285-116">Parent elements</span></span>

|<span data-ttu-id="e0285-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e0285-117">**Element**</span></span>|<span data-ttu-id="e0285-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="e0285-118">**Type**</span></span>|<span data-ttu-id="e0285-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="e0285-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e0285-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="e0285-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="e0285-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="e0285-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e0285-122">Contient les éléments **DataConnection** pour le document.</span><span class="sxs-lookup"><span data-stu-id="e0285-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e0285-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e0285-123">Child elements</span></span>

<span data-ttu-id="e0285-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e0285-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0285-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="e0285-125">Attributes</span></span>

|<span data-ttu-id="e0285-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e0285-126">**Attribute**</span></span>|<span data-ttu-id="e0285-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="e0285-127">**Type**</span></span>|<span data-ttu-id="e0285-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e0285-128">**Required**</span></span>|<span data-ttu-id="e0285-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="e0285-129">**Description**</span></span>|<span data-ttu-id="e0285-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e0285-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e0285-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="e0285-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="e0285-132">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="e0285-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e0285-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0285-133">optional</span></span>  <br/> |<span data-ttu-id="e0285-134">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="e0285-134">The default value is false.</span></span> <span data-ttu-id="e0285-135">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="e0285-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="e0285-136">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="e0285-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e0285-137">Commande</span><span class="sxs-lookup"><span data-stu-id="e0285-137">Command</span></span>  <br/> |<span data-ttu-id="e0285-138">XSD : String</span><span class="sxs-lookup"><span data-stu-id="e0285-138">xsd:string</span></span>  <br/> |<span data-ttu-id="e0285-139">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0285-139">optional</span></span>  <br/> |<span data-ttu-id="e0285-140">La chaîne de commande utilisée pour interroger la source de données.</span><span class="sxs-lookup"><span data-stu-id="e0285-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="e0285-141">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="e0285-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0285-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e0285-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="e0285-143">XSD : String</span><span class="sxs-lookup"><span data-stu-id="e0285-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e0285-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0285-144">optional</span></span>  <br/> |<span data-ttu-id="e0285-145">La chaîne de connexion qui définit les paramètres nécessaires pour se connecter à une source de données.</span><span class="sxs-lookup"><span data-stu-id="e0285-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="e0285-146">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="e0285-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0285-147">FileName</span><span class="sxs-lookup"><span data-stu-id="e0285-147">FileName</span></span>  <br/> |<span data-ttu-id="e0285-148">XSD : String</span><span class="sxs-lookup"><span data-stu-id="e0285-148">xsd:string</span></span>  <br/> |<span data-ttu-id="e0285-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e0285-149">required</span></span>  <br/> |<span data-ttu-id="e0285-150">Le nom du fichier de connexion.</span><span class="sxs-lookup"><span data-stu-id="e0285-150">The name of the connection file.</span></span> <span data-ttu-id="e0285-151">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="e0285-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="e0285-152">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="e0285-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0285-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e0285-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="e0285-154">XSD : String</span><span class="sxs-lookup"><span data-stu-id="e0285-154">xsd:string</span></span>  <br/> |<span data-ttu-id="e0285-155">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0285-155">optional</span></span>  <br/> |<span data-ttu-id="e0285-156">Un nom fourni par l’utilisateur pour la connexion de données.</span><span class="sxs-lookup"><span data-stu-id="e0285-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="e0285-157">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="e0285-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0285-158">ID</span><span class="sxs-lookup"><span data-stu-id="e0285-158">ID</span></span>  <br/> |<span data-ttu-id="e0285-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e0285-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0285-160">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e0285-160">required</span></span>  <br/> |<span data-ttu-id="e0285-161">L’ID affecté par Visio pour une connexion donnée, unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="e0285-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="e0285-162">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e0285-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0285-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="e0285-163">Timeout</span></span>  <br/> |<span data-ttu-id="e0285-164">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e0285-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0285-165">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0285-165">optional</span></span>  <br/> |<span data-ttu-id="e0285-166">Le temps d’attente en minutes lors de la tentative d’établir une connexion avant l’abandon de la tentative.</span><span class="sxs-lookup"><span data-stu-id="e0285-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="e0285-167">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e0285-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   


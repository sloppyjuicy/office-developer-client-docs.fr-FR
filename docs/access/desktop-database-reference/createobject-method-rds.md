---
title: CreateObject, méthode (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295372"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="b25ef-102">CreateObject, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="b25ef-102">CreateObject method (RDS)</span></span>

<span data-ttu-id="b25ef-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b25ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b25ef-p101">Crée le proxy pour l'objet métier cible et retourne un pointeur vers ce proxy. Le proxy procède à l'empaquetage des données et à leur marshaling sur le stub côté serveur afin d'autoriser les communications avec l'objet métier et d'envoyer des requêtes et des données sur Internet. Pour les objets de composant in-process, aucun proxy n'est utilisé, seul un pointeur vers l'objet est fourni.</span><span class="sxs-lookup"><span data-stu-id="b25ef-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="b25ef-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b25ef-107">Syntax</span></span>

<span data-ttu-id="b25ef-108">RDS (Remote Data Service) prend en charge les protocoles suivants : HTTP, HTTPS (HTTP sur SSL), DCOM et in-process.</span><span class="sxs-lookup"><span data-stu-id="b25ef-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b25ef-109">Protocole</span><span class="sxs-lookup"><span data-stu-id="b25ef-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="b25ef-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b25ef-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b25ef-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="b25ef-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="b25ef-112">Définir<em>l’objet</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="b25ef-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b25ef-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b25ef-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b25ef-114">Définir<em>l’objet</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="b25ef-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b25ef-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="b25ef-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="b25ef-116">Définir<em>l’objet</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>computername</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="b25ef-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b25ef-117">In-process</span><span class="sxs-lookup"><span data-stu-id="b25ef-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="b25ef-118">Définir<em>l’objet</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; &quot; )</span><span class="sxs-lookup"><span data-stu-id="b25ef-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="b25ef-119">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b25ef-119">Parameters</span></span>

|<span data-ttu-id="b25ef-120">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b25ef-120">Parameter</span></span>|<span data-ttu-id="b25ef-121">Description</span><span class="sxs-lookup"><span data-stu-id="b25ef-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b25ef-122">*Object*</span><span class="sxs-lookup"><span data-stu-id="b25ef-122">*Object*</span></span> |<span data-ttu-id="b25ef-123">Variable objet correspondant à un objet du type spécifié dans *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="b25ef-123">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>|
|<span data-ttu-id="b25ef-124">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="b25ef-124">*DataSpace*</span></span> |<span data-ttu-id="b25ef-125">Variable objet représentant un objet [RDS.DataSpace](dataspace-object-rds.md) utilisé pour créer une instance du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="b25ef-125">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>|
|<span data-ttu-id="b25ef-126">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="b25ef-126">*ProgID*</span></span> |<span data-ttu-id="b25ef-127">Valeur de type **String** contenant l'identificateur programmatique spécifiant un objet métier côté serveur qui implémente les règles métier de votre application.</span><span class="sxs-lookup"><span data-stu-id="b25ef-127">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>|
|<span data-ttu-id="b25ef-128">*awebsrvr* ou *computername*</span><span class="sxs-lookup"><span data-stu-id="b25ef-128">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="b25ef-129">Valeur de type **String** qui représente une URL identifiant le serveur web IIS (Internet Information Services) où une instance de l’objet métier serveur est créée.</span><span class="sxs-lookup"><span data-stu-id="b25ef-129">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b25ef-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="b25ef-130">Remarks</span></span>

<span data-ttu-id="b25ef-131">Le *protocole HTTP* est le protocole web standard ; *HTTPS* est un protocole web sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b25ef-131">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="b25ef-132">Utilisez le *protocole DCOM* en cas d'exécution sur un réseau local sans protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="b25ef-132">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="b25ef-133">Le protocole *in-process* est une bibliothèque DLL locale et n'utilise pas de réseau.</span><span class="sxs-lookup"><span data-stu-id="b25ef-133">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>


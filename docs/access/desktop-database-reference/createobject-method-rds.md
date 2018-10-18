---
title: CreateObject, méthode (RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ff2381626e8cf81aa95ee9d49f9396bd4b0316
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602719"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="22c02-102">CreateObject, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="22c02-102">CreateObject Method (RDS)</span></span>


<span data-ttu-id="22c02-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="22c02-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="22c02-p101">Crée le proxy pour l'objet métier cible et retourne un pointeur vers ce proxy. Le proxy procède à l'empaquetage des données et à leur marshaling sur le stub côté serveur afin d'autoriser les communications avec l'objet métier et d'envoyer des requêtes et des données sur Internet. Pour les objets de composant in-process, aucun proxy n'est utilisé, seul un pointeur vers l'objet est fourni.</span><span class="sxs-lookup"><span data-stu-id="22c02-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c02-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22c02-107">Syntax</span></span>

<span data-ttu-id="22c02-108">RDS (Remote Data Service) prend en charge les protocoles suivants : HTTP, HTTPS (HTTP sur SSL), DCOM et in-process.</span><span class="sxs-lookup"><span data-stu-id="22c02-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22c02-109">Protocole</span><span class="sxs-lookup"><span data-stu-id="22c02-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="22c02-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22c02-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22c02-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="22c02-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="22c02-112">Définir<em>l’objet</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="22c02-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c02-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="22c02-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="22c02-114">Définir<em>l’objet</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="22c02-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c02-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="22c02-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="22c02-116">Définir<em>l’objet</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>nom_ordinateur</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="22c02-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c02-117">In-process</span><span class="sxs-lookup"><span data-stu-id="22c02-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="22c02-118">Définir<em>l’objet</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="22c02-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="22c02-119">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22c02-119">Parameters</span></span>

  - <span data-ttu-id="22c02-120">*Object*</span><span class="sxs-lookup"><span data-stu-id="22c02-120">*Object*</span></span>

  - <span data-ttu-id="22c02-121">Variable objet correspondant à un objet du type spécifié dans *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="22c02-121">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>

  - <span data-ttu-id="22c02-122">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="22c02-122">*DataSpace*</span></span>

  - <span data-ttu-id="22c02-123">Variable objet représentant un objet [RDS.DataSpace](dataspace-object-rds.md) utilisé pour créer une instance du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="22c02-123">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>

  - <span data-ttu-id="22c02-124">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="22c02-124">*ProgID*</span></span>

  - <span data-ttu-id="22c02-125">Valeur de type **String** contenant l'identificateur programmatique spécifiant un objet métier côté serveur qui implémente les règles métier de votre application.</span><span class="sxs-lookup"><span data-stu-id="22c02-125">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>

  - <span data-ttu-id="22c02-126">*awebsrvr* ou *computername*</span><span class="sxs-lookup"><span data-stu-id="22c02-126">*awebsrvr* or *computername*</span></span>

<span data-ttu-id="22c02-127"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="22c02-127"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="22c02-128">Valeur de type **String** représentant une URL qui identifie le serveur Web IIS sur lequel une instance de l'objet métier du serveur est créée.</span><span class="sxs-lookup"><span data-stu-id="22c02-128">A **String** value that represents a URL identifying the Internet Information Services (IIS) Web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="22c02-129">Notes</span><span class="sxs-lookup"><span data-stu-id="22c02-129">Remarks</span></span>

<a name="the-http-protocol-is-the-standard-web-protocol-https-is-a-secure-web-protocol-use-the-dcom-protocol-when-running-a-local-area-network-without-http-the-in-process-protocol-is-a-local-dynamic-link-library-dll-it-does-not-use-a-network"></a><span data-ttu-id="22c02-130">Le *protocole HTTP* est le protocole Web standard ; *HTTPS* est un protocole Web sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22c02-130">The *HTTP protocol* is the standard Web protocol; *HTTPS* is a secure Web protocol.</span></span> <span data-ttu-id="22c02-131">Utiliser le *protocole DCOM* lors de l’exécution d’un réseau local sans protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="22c02-131">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="22c02-132">Le protocole *in-process* est une bibliothèque de liens dynamiques (DLL) ; locale Il n’utilise pas un réseau.</span><span class="sxs-lookup"><span data-stu-id="22c02-132">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>
=======
  - <span data-ttu-id="22c02-133">Une valeur de **type String** qui représente une URL qui identifie le serveur web Internet Information Services (IIS) où une instance de l’objet métier du serveur est créée.</span><span class="sxs-lookup"><span data-stu-id="22c02-133">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="22c02-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="22c02-134">Remarks</span></span>

<span data-ttu-id="22c02-135">Le *protocole HTTP* est le protocole web standard ; *HTTPS* est un protocole web sécurisé.</span><span class="sxs-lookup"><span data-stu-id="22c02-135">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="22c02-136">Utiliser le *protocole DCOM* lors de l’exécution d’un réseau local sans protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="22c02-136">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="22c02-137">Le protocole *in-process* est une bibliothèque de liens dynamiques (DLL) ; locale Il n’utilise pas un réseau.</span><span class="sxs-lookup"><span data-stu-id="22c02-137">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>
>>>>>>> <span data-ttu-id="22c02-138">master</span><span class="sxs-lookup"><span data-stu-id="22c02-138">master</span></span>


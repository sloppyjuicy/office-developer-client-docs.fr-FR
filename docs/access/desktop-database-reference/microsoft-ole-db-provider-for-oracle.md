---
title: Fournisseur Microsoft OLE DB pour Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b9b506f40039ff91a6b1985606322fd86a9e7c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288931"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="177fc-102">Fournisseur Microsoft OLE DB pour Oracle</span><span class="sxs-lookup"><span data-stu-id="177fc-102">Microsoft OLE DB Provider for Oracle</span></span>

<span data-ttu-id="177fc-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="177fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="177fc-104">Le fournisseur Microsoft OLE DB pour Oracle permet à ADO d'accéder aux bases de données Oracle.</span><span class="sxs-lookup"><span data-stu-id="177fc-104">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="177fc-105">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="177fc-105">Connection String Parameters</span></span>

<span data-ttu-id="177fc-106">Pour vous connecter à ce fournisseur, définissez l’argument *Provider* de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="177fc-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAORA 
```

<span data-ttu-id="177fc-107">La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="177fc-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

<span data-ttu-id="177fc-p101">Si une requête de jointure avec un keyset ou un curseur dynamique est exécutée dans une base de données Oracle, une erreur se produit. Oracle ne prend en charge qu'un curseur statique en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="177fc-p101">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs. Oracle only supports a static read-only cursor.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="177fc-110">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="177fc-110">Typical Connection String</span></span>

<span data-ttu-id="177fc-111">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="177fc-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

<span data-ttu-id="177fc-112">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="177fc-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="177fc-113">Mot clé</span><span class="sxs-lookup"><span data-stu-id="177fc-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="177fc-114">Description</span><span class="sxs-lookup"><span data-stu-id="177fc-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="177fc-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="177fc-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="177fc-116">Spécifie le fournisseur Microsoft OLE DB pour Oracle.</span><span class="sxs-lookup"><span data-stu-id="177fc-116">Specifies the OLE DB Provider for Oracle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="177fc-117"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="177fc-117"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="177fc-118">Spécifie le nom d'un serveur.</span><span class="sxs-lookup"><span data-stu-id="177fc-118">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="177fc-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="177fc-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="177fc-120">Spécifie le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="177fc-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="177fc-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="177fc-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="177fc-122">Spécifie le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="177fc-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="177fc-123">Paramètres de connexion spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="177fc-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="177fc-p102">Le fournisseur prend en charge plusieurs paramètres de connexion qui lui sont spécifiques en plus de ceux définis par ADO. Comme les propriétés de connexion ADO, ces propriétés spécifiques au fournisseur peuvent être définies via la collection [Properties](properties-collection-ado.md) d'un objet [Connection](connection-object-ado.md) ou dans **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="177fc-p102">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or as part of the **ConnectionString**.</span></span>

<span data-ttu-id="177fc-p103">Ces paramètres sont décrits en détail dans le guide OLE DB Programmer's Reference (en anglais). (L'[Index des propriétés dynamiques ADO](ado-dynamic-property-index.md) est un index croisé de ces noms de paramètres et des propriétés OLE DB correspondantes.)</span><span class="sxs-lookup"><span data-stu-id="177fc-p103">These parameters are fully described in the OLE DB Programmer's Reference. (The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between these parameter names and the corresponding OLE DB properties.)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="177fc-128">Paramètre</span><span class="sxs-lookup"><span data-stu-id="177fc-128">Parameter</span></span></p></th>
<th><p><span data-ttu-id="177fc-129">Description</span><span class="sxs-lookup"><span data-stu-id="177fc-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="177fc-130"><strong>Window Handle</strong></span><span class="sxs-lookup"><span data-stu-id="177fc-130"><strong>Window Handle</strong></span></span></p></td>
<td><p><span data-ttu-id="177fc-131">Indique le descripteur de fenêtre à utiliser pour solliciter d'autres informations.</span><span class="sxs-lookup"><span data-stu-id="177fc-131">Indicates the window handle to use to prompt for additional information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="177fc-132"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="177fc-132"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="177fc-p104">Spécifie un nombre 32 bits unique (par exemple, 1033) qui indique les préférences relatives à la langue de l'utilisateur. Ces préférences décrivent le format de la date et de l'heure, l'ordre alphabétique utilisé pour trier les éléments, le mode de comparaison des chaînes, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="177fc-p104">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="177fc-135"><strong>OLE DB Services</strong></span><span class="sxs-lookup"><span data-stu-id="177fc-135"><strong>OLE DB Services</strong></span></span></p></td>
<td><p><span data-ttu-id="177fc-136">Spécifie un masque de bits qui indique les services OLE DB à activer et à désactiver.</span><span class="sxs-lookup"><span data-stu-id="177fc-136">Indicates a bitmask that specifies OLE DB services to enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="177fc-137"><strong>Prompt</strong></span><span class="sxs-lookup"><span data-stu-id="177fc-137"><strong>Prompt</strong></span></span></p></td>
<td><p><span data-ttu-id="177fc-138">Indique s'il faut envoyer une invite à l'utilisateur lors de l'établissement d'une connexion.</span><span class="sxs-lookup"><span data-stu-id="177fc-138">Indicates whether to prompt the user while a connection is being established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="177fc-139"><strong>Extended Properties</strong></span><span class="sxs-lookup"><span data-stu-id="177fc-139"><strong>Extended Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="177fc-140">Chaîne contenant des informations de connexion étendues spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="177fc-140">A string containing provider-specific, extended connection information.</span></span> <span data-ttu-id="177fc-141">Utilisez cette propriété pour obtenir des informations de connexion spécifiques au fournisseur qui ne peuvent pas être décrites via le mécanisme de propriété.</span><span class="sxs-lookup"><span data-stu-id="177fc-141">Use this property only for provider-specific connection information that cannot be described through the property mechanism.</span></span></p></td>
</tr>
</tbody>
</table>


---
title: Objet DataSpace (RDS)
TOCTitle: DataSpace object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f77617d4ddfb0160b8a418f55582a380067fde70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294462"
---
# <a name="dataspace-object-rds"></a><span data-ttu-id="25af5-102">Objet DataSpace (RDS)</span><span class="sxs-lookup"><span data-stu-id="25af5-102">DataSpace object (RDS)</span></span>

<span data-ttu-id="25af5-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="25af5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25af5-104">Crée des proxys côté client pour les objets métier personnalisés de la couche intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="25af5-104">Creates client-side proxies to custom business objects located on the middle tier.</span></span>

## <a name="remarks"></a><span data-ttu-id="25af5-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="25af5-105">Remarks</span></span>

<span data-ttu-id="25af5-p101">Remote Data Service nécessite des proxys d'objets métier pour que le composant côté client puisse communiquer avec des objets métier situés au niveau intermédiaire. Les proxys permettent l'assemblage, le désassemblage et le transport (marshaling) des données de [Recordset](recordset-object-ado.md) d'une application pour qu'elles puissent franchir les frontières des processus et des machines.</span><span class="sxs-lookup"><span data-stu-id="25af5-p101">Remote Data Service needs business object proxies so that client-side component can communicate with business objects located on the middle tier. Proxies facilitate the packaging, unpackaging, and transport (marshaling) of the application's [Recordset](recordset-object-ado.md) data across process or machine boundaries.</span></span>

<span data-ttu-id="25af5-p102">Remote Data Service utilise la méthode **CreateObject** de l'objet [RDS.DataSpace](createobject-method-rds.md) pour créer des proxys d'objet métier. Un proxy d'objet métier est créé de manière dynamique chaque fois qu'une instance de son objet métier équivalent de niveau intermédiaire est créée. Remote Data Service prend en charge les protocoles suivants : HTTP, HTTPS (HTTP Secure Sockets), DCOM et in-process (les composants clients et l'objet métier résident sur le même ordinateur).</span><span class="sxs-lookup"><span data-stu-id="25af5-p102">Remote Data Service uses the **RDS.DataSpace** object's [CreateObject](createobject-method-rds.md) method to create business object proxies. The business object proxy is dynamically created whenever an instance of its middle-tier business object counterpart is created. Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP Secure Sockets), DCOM, and in-process (client components and the business object reside on the same computer).</span></span>

> [!NOTE]
> <span data-ttu-id="25af5-p103">[!REMARQUE] RDS fonctionne « sans état » lorsque l'objet **RDS.DataSpace** utilise les protocoles HTTP ou HTTPS. En d'autres termes, toute information interne concernant une demande client est ignorée après le renvoi d'une réponse par le serveur.</span><span class="sxs-lookup"><span data-stu-id="25af5-p103">RDS behaves in a "stateless" manner when the **RDS.DataSpace** object uses the HTTP or HTTPS protocols. That is, any internal information about a client request is discarded after the server returns a response.</span></span>

<span data-ttu-id="25af5-p104">Bien que l'objet métier semble exister pendant la durée du vie du proxy d'objet métier, il n'existe en fait que jusqu'à ce qu'une réponse à la demande soit envoyée. Lorsqu'une demande est émise (quand une méthode est appelée pour l'objet métier), le proxy ouvre une nouvelle connexion sur le serveur et ce dernier crée une nouvelle instance de l'objet métier. Lorsque ce dernier a répondu à la demande, le serveur le détruit et ferme la connexion.</span><span class="sxs-lookup"><span data-stu-id="25af5-p104">Although the business object appears to exist for the lifetime of the business object proxy, the business object actually exists only until a response is sent to a request. When a request is issued (that is, a method is invoked on the business object), the proxy opens a new connection to the server and the server creates a new instance of the business object. After the business object responds to the request, the server destroys the business object and closes the connection.</span></span>

<span data-ttu-id="25af5-p105">Ce comportement signifie que vous ne pouvez pas passer de données d'une demande à une autre à l'aide d'une propriété ou d'une variable de l'objet métier. Vous devez utiliser un autre mécanisme, comme un fichier ou un argument de méthode, pour rendre persistantes les données d'état.</span><span class="sxs-lookup"><span data-stu-id="25af5-p105">This behavior means you cannot pass data from one request to another using a business object property or variable. You must employ some other mechanism, such as a file or a method argument, to persist state data.</span></span>

<span data-ttu-id="25af5-118">L'identificateur de classe (Class ID) de l'objet **RDS.DataControl** est BD96C556-65A3-11D0-983A-00C04FC29E36.</span><span class="sxs-lookup"><span data-stu-id="25af5-118">The class ID for the **RDS.DataSpace** object is BD96C556-65A3-11D0-983A-00C04FC29E36.</span></span>


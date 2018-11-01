---
title: Provider, propriété (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df764aca267cab9b38760c432cd19154d6c6827f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881565"
---
# <a name="provider-property-ado"></a><span data-ttu-id="bd847-102">Provider, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd847-102">Provider property (ADO)</span></span>


<span data-ttu-id="bd847-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd847-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd847-104">Indique le nom du fournisseur d'un objet [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bd847-104">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="bd847-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bd847-105">Settings and return values</span></span>

<span data-ttu-id="bd847-106">Définit ou renvoie une valeur **String** qui indique le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bd847-106">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd847-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="bd847-107">Remarks</span></span>

<span data-ttu-id="bd847-p101">Utilisez la propriété **Provider** pour définir ou renvoyer le nom du fournisseur d’une connexion. Cette propriété peut aussi être définie par le contenu de la propriété [ConnectionString](connectionstring-property-ado.md) ou de l’argument *ConnectionString* de la méthode [Open](open-method-ado-connection.md). Toutefois, si l’on indique le fournisseur à plusieurs endroits et que l’on appelle la méthode **Open**, les résultats sont imprévisibles. Si aucun fournisseur n’est spécifié, la valeur par défaut de la propriété est MSDASQL ([Fournisseur Microsoft OLE DB pour ODBC](microsoft-ole-db-provider-for-odbc.md)).</span><span class="sxs-lookup"><span data-stu-id="bd847-p101">Use the **Provider** property to set or return the name of the provider for a connection. This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results. If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="bd847-p102">La propriété **Provider** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte. Le paramètre ne prend que lorsque l'on ouvre l'objet **Connection** ou que l'on accède à la collection [Properties](properties-collection-ado.md) de l'objet **Connection**. Si le paramètre n'est pas valide, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="bd847-p102">The **Provider** property is read/write when the connection is closed and read-only when it is open. The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object. If the setting is not valid, an error occurs.</span></span>


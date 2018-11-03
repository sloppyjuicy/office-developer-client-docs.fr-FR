---
title: Source, propriété (objet Record ADO)
TOCTitle: Source property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b41521ac3b4ba0f07eac188a7103025be2800e4d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946502"
---
# <a name="source-property-ado-record"></a><span data-ttu-id="850c1-102">Source, propriété (objet Record ADO)</span><span class="sxs-lookup"><span data-stu-id="850c1-102">Source property (ADO Record)</span></span>


<span data-ttu-id="850c1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="850c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="850c1-104">Indique la source de données ou l'objet que représente l'objet [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="850c1-104">Indicates the data source or object represented by the [Record](record-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="850c1-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="850c1-105">Settings and return values</span></span>

<span data-ttu-id="850c1-106">Définit ou renvoie une valeur **Variant** qui indique l'entité que représente l'objet **Record**.</span><span class="sxs-lookup"><span data-stu-id="850c1-106">Sets or returns a **Variant** value that indicates the entity represented by the **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="850c1-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="850c1-107">Remarks</span></span>

<span data-ttu-id="850c1-108">La propriété **Source** renvoie l’argument *Source* de la méthode [Open](open-method-ado-record.md) de l’objet **Record** .</span><span class="sxs-lookup"><span data-stu-id="850c1-108">The **Source** property returns the *Source* argument of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="850c1-109">Elle peut contenir une chaîne représentant une URL absolue ou relative.</span><span class="sxs-lookup"><span data-stu-id="850c1-109">It can contain an absolute or relative URL string.</span></span> <span data-ttu-id="850c1-110">Une URL absolue peut être utilisée sans que la propriété [ActiveConnection](activeconnection-property-ado.md) ne soit définie pour ouvrir directement l'objet **Record**.</span><span class="sxs-lookup"><span data-stu-id="850c1-110">An absolute URL can be used without setting the [ActiveConnection](activeconnection-property-ado.md) property to directly open the **Record** object.</span></span> <span data-ttu-id="850c1-111">Dans ce cas, un objet **Connection** implicite est créé.</span><span class="sxs-lookup"><span data-stu-id="850c1-111">An implicit **Connection** object is created in this case.</span></span>

<span data-ttu-id="850c1-112">La propriété **Source** peut également contenir une référence à un **Recordset** déjà ouvert, ce qui ouvre un objet **Record** représentant la ligne actuelle dans le **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="850c1-112">The **Source** property can also contain a reference to an already open **Recordset**, which opens a **Record** object representing the current row in the **Recordset**.</span></span>

<span data-ttu-id="850c1-113">La propriété **Source** peut également contenir une référence à un objet [Command](command-object-ado.md) qui renvoie du fournisseur une seule ligne de données.</span><span class="sxs-lookup"><span data-stu-id="850c1-113">The **Source** property could also contain a reference to a [Command](command-object-ado.md) object which returns a single row of data from the provider.</span></span>

<span data-ttu-id="850c1-p102">Si la propriété **ActiveConnection** est elle aussi définie, la propriété **Source** doit pointer vers un objet à la portée de cette connexion. Par exemple, dans les espaces de noms structurés en arborescence, si la propriété **Source** contient une URL absolue, elle doit par exemple pointer vers un nœud à la portée du nœud identifié par l'URL dans la chaîne de connexion. Si la propriété **Source** contient une URL relative, cette URL est validée dans le contexte défini par la propriété **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="850c1-p102">If the **ActiveConnection** property is also set, then the **Source** property must point to some object that exists within the scope of that connection. For example, in tree-structured namespaces, if the **Source** property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string. If the **Source** property contains a relative URL, then it is validated within the context set by the **ActiveConnection** property.</span></span>

<span data-ttu-id="850c1-117">La propriété **Source** est accessible en lecture/écriture lorsque l'objet **Record** est fermé et en lecture seule lorsque l'objet **Record** est ouvert.</span><span class="sxs-lookup"><span data-stu-id="850c1-117">The **Source** property is read/write while the **Record** object is closed, and is read-only while the **Record** object is open.</span></span>

> [!NOTE]
> <span data-ttu-id="850c1-118">[!REMARQUE] Les URL construites sur le schéma http invoquent automatiquement le [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="850c1-118">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="850c1-119">Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="850c1-119">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>



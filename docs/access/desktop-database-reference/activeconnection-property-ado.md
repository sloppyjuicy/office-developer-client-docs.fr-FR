---
title: ActiveConnection, propriété (ADO)
TOCTitle: ActiveConnection Property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d44a17d192abdb68755a2010184b4fb4d6531174
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472513"
---
# <a name="activeconnection-property-ado"></a><span data-ttu-id="17d30-102">ActiveConnection, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="17d30-102">ActiveConnection Property (ADO)</span></span>


<span data-ttu-id="17d30-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="17d30-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="17d30-104">Indique l'objet [Connection](connection-object-ado.md) auquel l'objet [Command](command-object-ado.md), [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md) spécifié appartient actuellement.</span><span class="sxs-lookup"><span data-stu-id="17d30-104">Indicates to which [Connection](connection-object-ado.md) object the specified [Command](command-object-ado.md), [Recordset](recordset-object-ado.md), or [Record](record-object-ado.md) object currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="17d30-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="17d30-105">Settings and Return Values</span></span>

<span data-ttu-id="17d30-p101">Définit ou renvoie une valeur de type **String** contenant la définition d'une connexion si la connexion est fermée, ou une valeur **Variant** contenant l'objet **Connection** actif si la connexion est ouverte. La valeur par défaut est une référence d'objet Null. Reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="17d30-p101">Sets or returns a **String** value that contains a definition for a connection if the connection is closed, or a **Variant** containing the current **Connection** object if the connection is open. Default is a null object reference. See the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d30-109">Notes</span><span class="sxs-lookup"><span data-stu-id="17d30-109">Remarks</span></span>

<span data-ttu-id="17d30-110">Utilisez la propriété **ActiveConnection** pour déterminer l'objet **Connection** sur lequel l'objet **Command** est exécuté ou sur lequel l'objet **Recordset** spécifié est ouvert.</span><span class="sxs-lookup"><span data-stu-id="17d30-110">Use the **ActiveConnection** property to determine the **Connection** object over which the specified **Command** object will execute or the specified **Recordset** will be opened.</span></span>

<span data-ttu-id="17d30-111">**Command**</span><span class="sxs-lookup"><span data-stu-id="17d30-111">**Command**</span></span>

<span data-ttu-id="17d30-112">Pour les objets **Command**, la propriété **ActiveConnection** est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="17d30-112">For **Command** objects, the **ActiveConnection** property is read/write.</span></span>

<span data-ttu-id="17d30-113">Si vous tentez d'appeler la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) sur un objet **Command** avant d'affecter à cette propriété un objet **Connection** ouvert ou une chaîne de connexion valide, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="17d30-113">If you attempt to call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method on a **Command** object before setting this property to an open **Connection** object or valid connection string, an error occurs.</span></span>

<span data-ttu-id="17d30-114">**Microsoft Visual Basic** Si la propriété **ActiveConnection** sur *Nothing* dissocie l’objet **Command** à partir de la **connexion** en cours et le fournisseur libérer les ressources associées dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="17d30-114">**Microsoft Visual Basic**Setting the **ActiveConnection** property to *Nothing* disassociates the **Command** object from the current **Connection** and causes the provider to release any associated resources on the data source.</span></span> <span data-ttu-id="17d30-115">Vous pouvez alors associer l'objet **Command** au même objet **Connection** ou à un autre.</span><span class="sxs-lookup"><span data-stu-id="17d30-115">You can then associate the **Command** object with the same or another **Connection** object.</span></span> <span data-ttu-id="17d30-116">Certains fournisseurs permettent de modifier le paramètre de propriété d’une **connexion** à un autre, sans devoir tout d’abord définir la propriété sur *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="17d30-116">Some providers allow you to change the property setting from one **Connection** to another, without having to first set the property to *Nothing*.</span></span>

<span data-ttu-id="17d30-117">Si la collection [Parameters](parameters-collection-ado.md) de l’objet **Command** contient les paramètres fournis par le fournisseur, la collection est effacée si vous définissez la propriété **ActiveConnection** sur *Nothing* ou sur un autre objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="17d30-117">If the [Parameters](parameters-collection-ado.md) collection of the **Command** object contains parameters supplied by the provider, the collection is cleared if you set the **ActiveConnection** property to *Nothing* or to another **Connection** object.</span></span> <span data-ttu-id="17d30-118">Si vous créez des objets [Parameter](parameter-object-ado.md) et les utilisez pour remplir la collection **Parameters** de l’objet **Command** manuellement, paramètre **ActiveConnection** sur *Nothing* ou un autre objet **Connection** propriété quitte la collection **Parameters** intacte.</span><span class="sxs-lookup"><span data-stu-id="17d30-118">If you manually create [Parameter](parameter-object-ado.md) objects and use them to fill the **Parameters** collection of the **Command** object, setting the **ActiveConnection** property to *Nothing* or to another **Connection** object leaves the **Parameters** collection intact.</span></span>

<span data-ttu-id="17d30-p104">La fermeture de l'objet **Connection** auquel est associé un objet **Command** affecte à la propriété **ActiveConnection** la valeur *Nothing*. L'attribution d'un objet **Connection** fermé à cette propriété génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="17d30-p104">Closing the **Connection** object with which a **Command** object is associated sets the **ActiveConnection** property to *Nothing*. Setting this property to a closed **Connection** object generates an error.</span></span>

<span data-ttu-id="17d30-121">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="17d30-121">**Recordset**</span></span>

<span data-ttu-id="17d30-p105">Pour les objets **Recordset** ouverts ou pour les objets **Recordset** dont la propriété [Source](source-property-ado-recordset.md) a pour valeur un objet **Command** valide, la propriété **ActiveConnection** est en lecture seule. Autrement, elle est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="17d30-p105">For open **Recordset** objects or for **Recordset** objects whose [Source](source-property-ado-recordset.md) property is set to a valid **Command** object, the **ActiveConnection** property is read-only. Otherwise, it is read/write.</span></span>

<span data-ttu-id="17d30-p106">Vous pouvez affecter à cette propriété un objet **Connection** valide ou une chaîne de connexion valide. Dans ce cas, le fournisseur crée un objet **Connection** à l'aide de cette définition et ouvre la connexion. De plus, le fournisseur peut définir cette propriété sur le nouvel objet **Connection** pour vous permettre d'accéder à l'objet **Connection** et obtenir des informations complémentaires relatives à l'objet ou exécuter d'autres commandes.</span><span class="sxs-lookup"><span data-stu-id="17d30-p106">You can set this property to a valid **Connection** object or to a valid connection string. In this case, the provider creates a new **Connection** object using this definition and opens the connection. Additionally, the provider may set this property to the new **Connection** object to give you a way to access the **Connection** object for extended error information or to execute other commands.</span></span>

<span data-ttu-id="17d30-127">Si vous utilisez l’argument *ActiveConnection* de la méthode [Open](open-method-ado-recordset.md) pour ouvrir un objet **Recordset** , la propriété **ActiveConnection** héritera de la valeur de l’argument.</span><span class="sxs-lookup"><span data-stu-id="17d30-127">If you use the *ActiveConnection* argument of the [Open](open-method-ado-recordset.md) method to open a **Recordset** object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="17d30-128">Si vous affectez à la propriété **Source** de l'objet **Recordset** une variable d'objet **Command** valide, la propriété **ActiveConnection** de l'objet **Recordset** hérite du paramètre de la propriété **ActiveConnection** de l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="17d30-128">If you set the **Source** property of the **Recordset** object to a valid **Command** object variable, the **ActiveConnection** property of the **Recordset** inherits the setting of the **Command** object's **ActiveConnection** property.</span></span>

<span data-ttu-id="17d30-129">**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet Recordset de côté client, cette propriété peut être définie qu’une chaîne de connexion ou (dans Microsoft Visual Basic ou Visual Basic, Scripting Edition) *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="17d30-129">**Remote Data Service Usage**When used on a client-side Recordset object, this property can be set only to a connection string or (in Microsoft Visual Basic or Visual Basic, Scripting Edition) to *Nothing*.</span></span>

<span data-ttu-id="17d30-130">**Record**</span><span class="sxs-lookup"><span data-stu-id="17d30-130">**Record**</span></span>

<span data-ttu-id="17d30-p107">Cette propriété est en lecture/écriture lorsque l'objet **Record** est fermé et peut contenir une chaîne de connexion ou une référence à un objet **Connection** ouvert. Cette propriété est en lecture seule lorsque l'objet **Record** est ouvert et qu'il contient une référence à un objet **Connection** ouvert.</span><span class="sxs-lookup"><span data-stu-id="17d30-p107">This property is read/write when the **Record** object is closed, and may contain a connection string or reference to an open **Connection** object. This property is read-only when the **Record** object is open, and contains a reference to an open **Connection** object.</span></span>

<span data-ttu-id="17d30-p108">Un objet **Connection** est créé implicitement lorsque l'objet **Record** est ouvert à partir d'une URL. Ouvrez l'objet **Record** à l'aide d'un objet **Connection** existant ouvert en affectant à cette propriété l'objet **Connection** ou en utilisant l'objet **Connection** comme paramètre dans l'appel de la méthode [Open](open-method-ado-record.md). Si l'objet **Record** est ouvert à partir d'un objet **Record** ou [Recordset](recordset-object-ado.md) existant, il est automatiquement associé à l'objet **Connection** de cet objet **Record** ou **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="17d30-p108">A **Connection** object is created implicitly when the **Record** object is opened from a URL. Open the **Record** with an existing, open **Connection** object by assigning the **Connection** object to this property, or using the **Connection** object as a parameter in the [Open](open-method-ado-record.md) method call. If the **Record** is opened from an existing **Record** or [Recordset](recordset-object-ado.md), then it is automatically associated with that **Record** or **Recordset** object's **Connection** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="17d30-p109">[!REMARQUE] Les URL utilisant le schéma HTTP appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, reportez-vous à la section <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</span><span class="sxs-lookup"><span data-stu-id="17d30-p109">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>



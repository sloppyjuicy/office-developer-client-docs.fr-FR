---
title: ActiveConnection, propriété (ADO)
TOCTitle: ActiveConnection property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 10/17/2018
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 037ae753f427c42f147972170dbb2e645b260623
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282529"
---
# <a name="activeconnection-property-ado"></a><span data-ttu-id="17ca1-102">ActiveConnection, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="17ca1-102">ActiveConnection property (ADO)</span></span>

<span data-ttu-id="17ca1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17ca1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17ca1-104">Indique l'objet [Connection](connection-object-ado.md) auquel l'objet [Command](command-object-ado.md), [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md) spécifié appartient actuellement.</span><span class="sxs-lookup"><span data-stu-id="17ca1-104">Indicates to which [Connection](connection-object-ado.md) object the specified [Command](command-object-ado.md), [Recordset](recordset-object-ado.md), or [Record](record-object-ado.md) object currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="17ca1-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="17ca1-105">Settings and return values</span></span>

<span data-ttu-id="17ca1-p101">Définit ou renvoie une valeur de type **String** contenant la définition d'une connexion si la connexion est fermée, ou une valeur **Variant** contenant l'objet **Connection** actif si la connexion est ouverte. La valeur par défaut est une référence d'objet Null. Reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="17ca1-p101">Sets or returns a **String** value that contains a definition for a connection if the connection is closed, or a **Variant** containing the current **Connection** object if the connection is open. Default is a null object reference. See the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="17ca1-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="17ca1-109">Remarks</span></span>

<span data-ttu-id="17ca1-110">Utilisez la propriété **ActiveConnection** pour déterminer l'objet **Connection** sur lequel l'objet **Command** est exécuté ou sur lequel l'objet **Recordset** spécifié est ouvert.</span><span class="sxs-lookup"><span data-stu-id="17ca1-110">Use the **ActiveConnection** property to determine the **Connection** object over which the specified **Command** object will execute or the specified **Recordset** will be opened.</span></span>

### <a name="command"></a><span data-ttu-id="17ca1-111">Commande</span><span class="sxs-lookup"><span data-stu-id="17ca1-111">Command</span></span>

<span data-ttu-id="17ca1-112">Pour les objets **Command**, la propriété **ActiveConnection** est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="17ca1-112">For **Command** objects, the **ActiveConnection** property is read/write.</span></span>

<span data-ttu-id="17ca1-113">Si vous tentez d'appeler la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) sur un objet **Command** avant d'affecter à cette propriété un objet **Connection** ouvert ou une chaîne de connexion valide, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="17ca1-113">If you attempt to call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method on a **Command** object before setting this property to an open **Connection** object or valid connection string, an error occurs.</span></span>

<span data-ttu-id="17ca1-114">**Microsoft Visual Basic**: la définition de la propriété **ActiveConnection** sur *Nothing*  dissocie l’objet **Command** de la connexion actuelle et entraîne le fournisseur à libérer les ressources associées sur la source de données.</span><span class="sxs-lookup"><span data-stu-id="17ca1-114">**Microsoft Visual Basic**: Setting the **ActiveConnection** property to *Nothing* disassociates the **Command** object from the current **Connection** and causes the provider to release any associated resources on the data source.</span></span> <span data-ttu-id="17ca1-115">Vous pouvez alors associer l’objet **Command** au même objet **Connection** ou à un autre.</span><span class="sxs-lookup"><span data-stu-id="17ca1-115">You can then associate the **Command** object with the same or another **Connection** object.</span></span> <span data-ttu-id="17ca1-116">Certains fournisseurs permettent de remplacer l’objet **Connection** défini dans la propriété par un autre, sans devoir préalablement affecter à la propriété la valeur *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="17ca1-116">Some providers allow you to change the property setting from one **Connection** to another, without having to first set the property to *Nothing*.</span></span>

<span data-ttu-id="17ca1-p103">Si la collection [Parameters](parameters-collection-ado.md) de l’objet **Command** contient les paramètres fournis par le fournisseur, le contenu de la collection est effacé si vous attribuez à la propriété **ActiveConnection** la valeur *Nothing* ou un autre objet **Connection**. Si vous créez manuellement des objets [Parameter](parameter-object-ado.md) et que vous les utilisez pour remplir la collection **Parameters** de l’objet **Command**, l’affectation de la valeur *Nothing* ou d’un autre objet **Connection** à la propriété **ActiveConnection** ne modifie pas la collection **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="17ca1-p103">If the [Parameters](parameters-collection-ado.md) collection of the **Command** object contains parameters supplied by the provider, the collection is cleared if you set the **ActiveConnection** property to *Nothing* or to another **Connection** object. If you manually create [Parameter](parameter-object-ado.md) objects and use them to fill the **Parameters** collection of the **Command** object, setting the **ActiveConnection** property to *Nothing* or to another **Connection** object leaves the **Parameters** collection intact.</span></span>

<span data-ttu-id="17ca1-p104">La fermeture de l'objet **Connection** auquel est associé un objet **Command** affecte à la propriété **ActiveConnection** la valeur *Nothing*. L'attribution d'un objet **Connection** fermé à cette propriété génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="17ca1-p104">Closing the **Connection** object with which a **Command** object is associated sets the **ActiveConnection** property to *Nothing*. Setting this property to a closed **Connection** object generates an error.</span></span>

### <a name="recordset"></a><span data-ttu-id="17ca1-121">Recordset</span><span class="sxs-lookup"><span data-stu-id="17ca1-121">Recordset</span></span>

<span data-ttu-id="17ca1-p105">Pour les objets **Recordset** ouverts ou pour les objets **Recordset** dont la propriété [Source](source-property-ado-recordset.md) a pour valeur un objet **Command** valide, la propriété **ActiveConnection** est en lecture seule. Autrement, elle est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="17ca1-p105">For open **Recordset** objects or for **Recordset** objects whose [Source](source-property-ado-recordset.md) property is set to a valid **Command** object, the **ActiveConnection** property is read-only. Otherwise, it is read/write.</span></span>

<span data-ttu-id="17ca1-p106">Vous pouvez affecter à cette propriété un objet **Connection** valide ou une chaîne de connexion valide. Dans ce cas, le fournisseur crée un objet **Connection** à l'aide de cette définition et ouvre la connexion. De plus, le fournisseur peut définir cette propriété sur le nouvel objet **Connection** pour vous permettre d'accéder à l'objet **Connection** et obtenir des informations complémentaires relatives à l'objet ou exécuter d'autres commandes.</span><span class="sxs-lookup"><span data-stu-id="17ca1-p106">You can set this property to a valid **Connection** object or to a valid connection string. In this case, the provider creates a new **Connection** object using this definition and opens the connection. Additionally, the provider may set this property to the new **Connection** object to give you a way to access the **Connection** object for extended error information or to execute other commands.</span></span>

<span data-ttu-id="17ca1-127">Si vous utilisez l’argument *ActiveConnection* de la méthode [Open](open-method-ado-recordset.md) pour ouvrir un objet **Recordset**, la propriété **ActiveConnection** hérite de la valeur de l’argument.</span><span class="sxs-lookup"><span data-stu-id="17ca1-127">If you use the *ActiveConnection* argument of the [Open](open-method-ado-recordset.md) method to open a **Recordset** object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="17ca1-128">Si vous affectez à la propriété **Source** de l'objet **Recordset** une variable d'objet **Command** valide, la propriété **ActiveConnection** de l'objet **Recordset** hérite du paramètre de la propriété **ActiveConnection** de l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="17ca1-128">If you set the **Source** property of the **Recordset** object to a valid **Command** object variable, the **ActiveConnection** property of the **Recordset** inherits the setting of the **Command** object's **ActiveConnection** property.</span></span>

<span data-ttu-id="17ca1-129">**Utilisation** du service de données distant : lorsqu’elle est utilisée sur un objet Recordset côté client, cette propriété peut être définie uniquement sur une chaîne de connexion ou (dans Microsoft Visual Basic ou Visual Basic, Scripting Edition) sur *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="17ca1-129">**Remote Data Service Usage**: When used on a client-side Recordset object, this property can be set only to a connection string or (in Microsoft Visual Basic or Visual Basic, Scripting Edition) to *Nothing*.</span></span>

### <a name="record"></a><span data-ttu-id="17ca1-130">Record</span><span class="sxs-lookup"><span data-stu-id="17ca1-130">Record</span></span>

<span data-ttu-id="17ca1-p107">Cette propriété est en lecture/écriture lorsque l'objet **Record** est fermé et peut contenir une chaîne de connexion ou une référence à un objet **Connection** ouvert. Cette propriété est en lecture seule lorsque l'objet **Record** est ouvert et qu'il contient une référence à un objet **Connection** ouvert.</span><span class="sxs-lookup"><span data-stu-id="17ca1-p107">This property is read/write when the **Record** object is closed, and may contain a connection string or reference to an open **Connection** object. This property is read-only when the **Record** object is open, and contains a reference to an open **Connection** object.</span></span>

<span data-ttu-id="17ca1-133">Un objet **Connection** est créé implicitement lorsque l'objet **Record** est ouvert à partir d'une URL.</span><span class="sxs-lookup"><span data-stu-id="17ca1-133">A **Connection** object is created implicitly when the **Record** object is opened from a URL.</span></span> <span data-ttu-id="17ca1-134">Ouvrez l'objet **Record** à l'aide d'un objet **Connection** existant ouvert en affectant à cette propriété l'objet **Connection** ou en utilisant l'objet **Connection** comme paramètre dans l'appel de la méthode [Open](open-method-ado-record.md).</span><span class="sxs-lookup"><span data-stu-id="17ca1-134">Open the **Record** with an existing, open **Connection** object by assigning the **Connection** object to this property, or using the **Connection** object as a parameter in the [Open](open-method-ado-record.md) method call.</span></span> <span data-ttu-id="17ca1-135">Si **l’enregistrement** est ouvert à partir d’un objet **Record** ou [Recordset](recordset-object-ado.md)existant, il est automatiquement associé à l’objet Connection de cet objet **Record** ou **Recordset.** </span><span class="sxs-lookup"><span data-stu-id="17ca1-135">If the **Record** is opened from an existing **Record** or [Recordset](recordset-object-ado.md), it is automatically associated with that **Record** or **Recordset** object's **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="17ca1-136">Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="17ca1-136">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="17ca1-137">Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="17ca1-137">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>




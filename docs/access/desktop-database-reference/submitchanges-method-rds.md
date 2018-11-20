---
title: SubmitChanges, méthode (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b5c18aa12519e9206702eb2a152e6f0d084edc9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026343"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="a49f7-102">SubmitChanges, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="a49f7-102">SubmitChanges method (RDS)</span></span>

<span data-ttu-id="a49f7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a49f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a49f7-104">Envoie les modifications en attente de l'objet [Recordset](recordset-object-ado.md) actualisable et placé dans le cache local à la source de données spécifiée dans la propriété [Connect](connect-property-rds.md) de la propriété [URL](url-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="a49f7-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a49f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a49f7-105">Syntax</span></span>

<span data-ttu-id="a49f7-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="a49f7-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="a49f7-107">*DataFactory*. SubmitChanges*connexion* *jeu d’enregistrements*</span><span class="sxs-lookup"><span data-stu-id="a49f7-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="a49f7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a49f7-108">Parameters</span></span>

|<span data-ttu-id="a49f7-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a49f7-109">Parameter</span></span>|<span data-ttu-id="a49f7-110">Description</span><span class="sxs-lookup"><span data-stu-id="a49f7-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a49f7-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="a49f7-111">*DataControl*</span></span> |<span data-ttu-id="a49f7-112">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="a49f7-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="a49f7-113">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="a49f7-113">*DataFactory*</span></span> |<span data-ttu-id="a49f7-114">Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="a49f7-114">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="a49f7-115">*Connection*</span><span class="sxs-lookup"><span data-stu-id="a49f7-115">*Connection*</span></span> |<span data-ttu-id="a49f7-116">Valeur de type **String** représentant la connexion créée avec la propriété **Connect** de l'objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="a49f7-116">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>|
|<span data-ttu-id="a49f7-117">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="a49f7-117">*Recordset*</span></span> |<span data-ttu-id="a49f7-118">Variable objet représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a49f7-118">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a49f7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a49f7-119">Remarks</span></span>

<span data-ttu-id="a49f7-120">Les propriétés [Connect](connect-property-rds.md), [Server](server-property-rds.md) et [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) doivent être définies avant de pouvoir utiliser la méthode **SubmitChanges** avec l'objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="a49f7-120">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="a49f7-121">Si vous appelez la méthode [CancelUpdate](cancelupdate-method-rds.md) après avoir appelé **SubmitChanges** pour le même objet **Recordset**, l'appel **CancelUpdate** échoue car les modifications ont déjà été validées.</span><span class="sxs-lookup"><span data-stu-id="a49f7-121">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="a49f7-122">Seuls les enregistrements modifiés sont envoyés pour modification. Par ailleurs, soit toutes les modifications aboutissent, soit elles échouent toutes.</span><span class="sxs-lookup"><span data-stu-id="a49f7-122">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="a49f7-123">Vous pouvez utiliser **SubmitChanges** qu’avec l’objet **RDSServer.DataFactory** *par défaut* .</span><span class="sxs-lookup"><span data-stu-id="a49f7-123">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="a49f7-124">Les objets métier personnalisés ne peuvent pas utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a49f7-124">Custom business objects can't use this method.</span></span>

<span data-ttu-id="a49f7-125">Si la propriété **URL** a été définie, **SubmitChanges** envoie les modifications à l'emplacement indiqué par l'URL.</span><span class="sxs-lookup"><span data-stu-id="a49f7-125">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>


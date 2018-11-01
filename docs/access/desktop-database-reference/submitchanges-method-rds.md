---
title: SubmitChanges, méthode (RDS)
TOCTitle: SubmitChanges Method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 521728af91967d673a1c69f4e4812b0aaa73ce59
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883882"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="b1f18-102">SubmitChanges, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="b1f18-102">SubmitChanges Method (RDS)</span></span>


<span data-ttu-id="b1f18-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1f18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1f18-104">Envoie les modifications en attente de l'objet [Recordset](recordset-object-ado.md) actualisable et placé dans le cache local à la source de données spécifiée dans la propriété [Connect](connect-property-rds.md) de la propriété [URL](url-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="b1f18-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f18-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1f18-105">Syntax</span></span>

<span data-ttu-id="b1f18-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="b1f18-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="b1f18-107">*DataFactory*. SubmitChanges*connexion* *jeu d’enregistrements*</span><span class="sxs-lookup"><span data-stu-id="b1f18-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="b1f18-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1f18-108">Parameters</span></span>

  - <span data-ttu-id="b1f18-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b1f18-109">*DataControl*</span></span>

  - <span data-ttu-id="b1f18-110">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="b1f18-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="b1f18-111">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="b1f18-111">*DataFactory*</span></span>

  - <span data-ttu-id="b1f18-112">Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="b1f18-112">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="b1f18-113">*Connection*</span><span class="sxs-lookup"><span data-stu-id="b1f18-113">*Connection*</span></span>

  - <span data-ttu-id="b1f18-114">Valeur de type **String** représentant la connexion créée avec la propriété **Connect** de l'objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="b1f18-114">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>

  - <span data-ttu-id="b1f18-115">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="b1f18-115">*Recordset*</span></span>

  - <span data-ttu-id="b1f18-116">Variable objet représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b1f18-116">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1f18-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b1f18-117">Remarks</span></span>

<span data-ttu-id="b1f18-118">Les propriétés [Connect](connect-property-rds.md), [Server](server-property-rds.md) et [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) doivent être définies avant de pouvoir utiliser la méthode **SubmitChanges** avec l'objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="b1f18-118">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="b1f18-119">Si vous appelez la méthode [CancelUpdate](cancelupdate-method-rds.md) après avoir appelé **SubmitChanges** pour le même objet **Recordset**, l'appel **CancelUpdate** échoue car les modifications ont déjà été validées.</span><span class="sxs-lookup"><span data-stu-id="b1f18-119">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="b1f18-120">Seuls les enregistrements modifiés sont envoyés pour modification. Par ailleurs, soit toutes les modifications aboutissent, soit elles échouent toutes.</span><span class="sxs-lookup"><span data-stu-id="b1f18-120">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="b1f18-121">Vous pouvez utiliser **SubmitChanges** qu’avec l’objet **RDSServer.DataFactory** *par défaut* .</span><span class="sxs-lookup"><span data-stu-id="b1f18-121">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="b1f18-122">Les objets métier personnalisés ne peuvent pas utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b1f18-122">Custom business objects can't use this method.</span></span>

<span data-ttu-id="b1f18-123">Si la propriété **URL** a été définie, **SubmitChanges** envoie les modifications à l'emplacement indiqué par l'URL.</span><span class="sxs-lookup"><span data-stu-id="b1f18-123">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>


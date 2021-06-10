---
title: PROPRIÉTÉ URL (RDS - Référence de base de données de bureau Access)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313397"
---
# <a name="url-property-rds"></a><span data-ttu-id="28a6e-102">PROPRIÉTÉ URL (RDS)</span><span class="sxs-lookup"><span data-stu-id="28a6e-102">URL property (RDS)</span></span>

<span data-ttu-id="28a6e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28a6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28a6e-104">Indique une chaîne contenant une URL relative ou absolue.</span><span class="sxs-lookup"><span data-stu-id="28a6e-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="28a6e-105">Vous pouvez définir la propriété **URL** au moment de la création dans la balise OBJECT de l'objet [DataControl](datacontrol-object-rds.md) ou en mode exécution dans le code de script.</span><span class="sxs-lookup"><span data-stu-id="28a6e-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="28a6e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28a6e-106">Syntax</span></span>

<span data-ttu-id="28a6e-107">Moment de la conception \< : PARAM NAME="URL » VALUE="Server »\></span><span class="sxs-lookup"><span data-stu-id="28a6e-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="28a6e-108">Durée d’application : DataControl.URL="Server »</span><span class="sxs-lookup"><span data-stu-id="28a6e-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="28a6e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28a6e-109">Parameters</span></span>

|<span data-ttu-id="28a6e-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="28a6e-110">Parameter</span></span>|<span data-ttu-id="28a6e-111">Description</span><span class="sxs-lookup"><span data-stu-id="28a6e-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="28a6e-112">*Serveur*</span><span class="sxs-lookup"><span data-stu-id="28a6e-112">*Server*</span></span> |<span data-ttu-id="28a6e-113">Valeur **String** contenant une URL valide.</span><span class="sxs-lookup"><span data-stu-id="28a6e-113">A **String** value that contains a valid URL.</span></span>|
|<span data-ttu-id="28a6e-114">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="28a6e-114">*DataControl*</span></span> |<span data-ttu-id="28a6e-115">Variable d'objet représentant un objet **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="28a6e-115">An object variable that represents a **DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="28a6e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="28a6e-116">Remarks</span></span>

<span data-ttu-id="28a6e-p101">L'URL identifie généralement un fichier ASP (.asp) qui peut produire et renvoyer un [Recordset](recordset-object-ado.md). L'utilisateur peut ainsi obtenir un **Recordset** sans avoir à appeler l'objet serveur [DataFactory](datafactory-object-rdsserver.md) ou programmer un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="28a6e-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="28a6e-119">Si la propriété **URL** a été définie, [SubmitChanges](submitchanges-method-rds.md) soumettra des modifications à l'emplacement spécifié par l'URL.</span><span class="sxs-lookup"><span data-stu-id="28a6e-119">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>


---
title: URL, propriété (RDS - référence du bureau de la base de données Access)
TOCTitle: URL Property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8d1e524df8f1921f712f9dce174ab90ebd57325
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469060"
---
# <a name="url-property-rds"></a><span data-ttu-id="610a7-102">URL, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="610a7-102">URL Property (RDS)</span></span>


<span data-ttu-id="610a7-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="610a7-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="610a7-104">Indique une chaîne contenant une URL relative ou absolue.</span><span class="sxs-lookup"><span data-stu-id="610a7-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="610a7-105">Vous pouvez définir la propriété **URL** au moment de la création dans la balise OBJECT de l'objet [DataControl](datacontrol-object-rds.md) ou en mode exécution dans le code de script.</span><span class="sxs-lookup"><span data-stu-id="610a7-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="610a7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="610a7-106">Syntax</span></span>

<span data-ttu-id="610a7-107">Au moment du design : \<PARAM NAME = valeur « URL » = « Serveur »\></span><span class="sxs-lookup"><span data-stu-id="610a7-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="610a7-108">Temps d’exécution : DataControl.URL="Server »</span><span class="sxs-lookup"><span data-stu-id="610a7-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="610a7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="610a7-109">Parameters</span></span>

  - <span data-ttu-id="610a7-110">*Serveur*</span><span class="sxs-lookup"><span data-stu-id="610a7-110">*Server*</span></span>

  - <span data-ttu-id="610a7-111">Valeur **String** contenant une URL valide.</span><span class="sxs-lookup"><span data-stu-id="610a7-111">A **String** value that contains a valid URL.</span></span>

  - <span data-ttu-id="610a7-112">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="610a7-112">*DataControl*</span></span>

  - <span data-ttu-id="610a7-113">Variable d'objet représentant un objet **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="610a7-113">An object variable that represents a **DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="610a7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="610a7-114">Remarks</span></span>

<span data-ttu-id="610a7-p101">L'URL identifie généralement un fichier ASP (.asp) qui peut produire et renvoyer un [Recordset ](recordset-object-ado.md). L'utilisateur peut ainsi obtenir un **Recordset** sans avoir à appeler l'objet serveur [DataFactory](datafactory-object-rdsserver.md) ou programmer un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="610a7-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="610a7-117">Si la propriété **URL** a été définie, [SubmitChanges](submitchanges-method-rds.md) soumettra des modifications à l'emplacement spécifié par l'URL.</span><span class="sxs-lookup"><span data-stu-id="610a7-117">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>


---
title: URL, propriété (RDS - référence du bureau de la base de données Access)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f75e5e1a6d4df21970eea387ecd85ac8ef346a70
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943772"
---
# <a name="url-property-rds"></a><span data-ttu-id="9cc95-102">URL, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="9cc95-102">URL property (RDS)</span></span>


<span data-ttu-id="9cc95-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9cc95-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="9cc95-104">Indique une chaîne contenant une URL relative ou absolue.</span><span class="sxs-lookup"><span data-stu-id="9cc95-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="9cc95-105">Vous pouvez définir la propriété **URL** au moment de la création dans la balise OBJECT de l'objet [DataControl](datacontrol-object-rds.md) ou en mode exécution dans le code de script.</span><span class="sxs-lookup"><span data-stu-id="9cc95-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc95-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9cc95-106">Syntax</span></span>

<span data-ttu-id="9cc95-107">Au moment du design : \<PARAM NAME = valeur « URL » = « Serveur »\></span><span class="sxs-lookup"><span data-stu-id="9cc95-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="9cc95-108">Temps d’exécution : DataControl.URL="Server »</span><span class="sxs-lookup"><span data-stu-id="9cc95-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="9cc95-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9cc95-109">Parameters</span></span>

- <span data-ttu-id="9cc95-110">*Serveur*</span><span class="sxs-lookup"><span data-stu-id="9cc95-110">*Server*</span></span>

  - <span data-ttu-id="9cc95-111">Valeur **String** contenant une URL valide.</span><span class="sxs-lookup"><span data-stu-id="9cc95-111">A **String** value that contains a valid URL.</span></span>

- <span data-ttu-id="9cc95-112">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="9cc95-112">*DataControl*</span></span>

  - <span data-ttu-id="9cc95-113">Variable d'objet représentant un objet **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="9cc95-113">An object variable that represents a **DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc95-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9cc95-114">Remarks</span></span>

<span data-ttu-id="9cc95-p101">L'URL identifie généralement un fichier ASP (.asp) qui peut produire et renvoyer un [Recordset ](recordset-object-ado.md). L'utilisateur peut ainsi obtenir un **Recordset** sans avoir à appeler l'objet serveur [DataFactory](datafactory-object-rdsserver.md) ou programmer un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9cc95-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="9cc95-117">Si la propriété **URL** a été définie, [SubmitChanges](submitchanges-method-rds.md) soumettra des modifications à l'emplacement spécifié par l'URL.</span><span class="sxs-lookup"><span data-stu-id="9cc95-117">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>


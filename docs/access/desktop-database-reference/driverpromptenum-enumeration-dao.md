---
title: DriverPromptEnum, énumération (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9612c0713a86ed6ad34a5eff61e45efcddf6cf24
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726105"
---
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="86776-102">DriverPromptEnum, énumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="86776-102">DriverPromptEnum enumeration (DAO)</span></span>


<span data-ttu-id="86776-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86776-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86776-104">Spécifie si le système doit demander à l'utilisateur d'établir une connexion et à quel moment cette demande doit avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="86776-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86776-105">Nom</span><span class="sxs-lookup"><span data-stu-id="86776-105">Name</span></span></p></th>
<th><p><span data-ttu-id="86776-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="86776-106">Value</span></span></p></th>
<th><p><span data-ttu-id="86776-107">Description</span><span class="sxs-lookup"><span data-stu-id="86776-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86776-108">dbDriverComplete</span><span class="sxs-lookup"><span data-stu-id="86776-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="86776-109">0</span><span class="sxs-lookup"><span data-stu-id="86776-109">0</span></span></p></td>
<td><p><span data-ttu-id="86776-110">Si la chaîne de connexion fournie comprend le mot clé DSN, le gestionnaire de pilotes utilise la chaîne comme indiqué dans Connect. Autrement, il se comporte comme lorsque <strong>dbDriverPrompt</strong> est spécifié.</span><span class="sxs-lookup"><span data-stu-id="86776-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86776-111">dbDriverCompleteRequired</span><span class="sxs-lookup"><span data-stu-id="86776-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="86776-112">3</span><span class="sxs-lookup"><span data-stu-id="86776-112">3</span></span></p></td>
<td><p><span data-ttu-id="86776-113">(Paramètre par défaut) Se comporte comme <strong>dbDriverComplete</strong>, excepté que le pilote désactive les contrôles pour les informations qui ne sont pas nécessaires à l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="86776-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86776-114">dbDriverNoPrompt</span><span class="sxs-lookup"><span data-stu-id="86776-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="86776-115">1</span><span class="sxs-lookup"><span data-stu-id="86776-115">1</span></span></p></td>
<td><p><span data-ttu-id="86776-p101">Le gestionnaire de pilotes utilise la chaîne de connexion fournie dans Connect. En l'absence d'informations détaillées, une erreur récupérable est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="86776-p101">The driver manager uses the connection string provided in connect. If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86776-118">dbDriverPrompt</span><span class="sxs-lookup"><span data-stu-id="86776-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="86776-119">2</span><span class="sxs-lookup"><span data-stu-id="86776-119">2</span></span></p></td>
<td><p><span data-ttu-id="86776-p102">Le gestionnaire de pilotes affiche la boîte de dialogue <strong>Sources de données ODBC</strong>. La chaîne de connexion utilisée pour établir la connexion est construite à partir du nom DSN sélectionné et fourni par l'utilisateur par le biais des boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="86776-p102">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box. The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>


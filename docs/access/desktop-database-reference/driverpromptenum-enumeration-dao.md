---
title: DriverPromptEnum Enumeration (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a69594ff30b92a32cf9ba95424ea7616df922725
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867439"
---
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="a5015-102">DriverPromptEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="a5015-102">DriverPromptEnum Enumeration (DAO)</span></span>


<span data-ttu-id="a5015-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5015-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a5015-104">Spécifie si le système doit demander à l'utilisateur d'établir une connexion et à quel moment cette demande doit avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="a5015-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5015-105">Nom</span><span class="sxs-lookup"><span data-stu-id="a5015-105">Name</span></span></p></th>
<th><p><span data-ttu-id="a5015-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5015-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a5015-107">Description</span><span class="sxs-lookup"><span data-stu-id="a5015-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5015-108">dbDriverComplete</span><span class="sxs-lookup"><span data-stu-id="a5015-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="a5015-109">0</span><span class="sxs-lookup"><span data-stu-id="a5015-109">0</span></span></p></td>
<td><p><span data-ttu-id="a5015-110">Si la chaîne de connexion fournie comprend le mot clé DSN, le gestionnaire de pilotes utilise la chaîne comme indiqué dans Connect. Autrement, il se comporte comme lorsque <strong>dbDriverPrompt</strong> est spécifié.</span><span class="sxs-lookup"><span data-stu-id="a5015-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5015-111">dbDriverCompleteRequired</span><span class="sxs-lookup"><span data-stu-id="a5015-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="a5015-112">3</span><span class="sxs-lookup"><span data-stu-id="a5015-112">3</span></span></p></td>
<td><p><span data-ttu-id="a5015-113">(Paramètre par défaut) Se comporte comme <strong>dbDriverComplete</strong>, excepté que le pilote désactive les contrôles pour les informations qui ne sont pas nécessaires à l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="a5015-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5015-114">dbDriverNoPrompt</span><span class="sxs-lookup"><span data-stu-id="a5015-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="a5015-115">1</span><span class="sxs-lookup"><span data-stu-id="a5015-115">1</span></span></p></td>
<td><p><span data-ttu-id="a5015-p101">Le gestionnaire de pilotes utilise la chaîne de connexion fournie dans Connect. En l'absence d'informations détaillées, une erreur récupérable est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="a5015-p101">The driver manager uses the connection string provided in connect. If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5015-118">dbDriverPrompt</span><span class="sxs-lookup"><span data-stu-id="a5015-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="a5015-119">2</span><span class="sxs-lookup"><span data-stu-id="a5015-119">2</span></span></p></td>
<td><p><span data-ttu-id="a5015-p102">Le gestionnaire de pilotes affiche la boîte de dialogue <strong>Sources de données ODBC</strong>. La chaîne de connexion utilisée pour établir la connexion est construite à partir du nom DSN sélectionné et fourni par l'utilisateur par le biais des boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a5015-p102">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box. The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>


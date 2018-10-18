---
title: Utilisation d'ADO avec des langages de script
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 196366987e89f52a3c498a769fa501a3faca9dae
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604434"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="db2ab-102">Utilisation d'ADO avec des langages de script</span><span class="sxs-lookup"><span data-stu-id="db2ab-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="db2ab-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="db2ab-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="db2ab-104"><<<<<<< Tête au sein d’un environnement de script, ADO permettent d’exposer des données via les scripts côté serveur.</span><span class="sxs-lookup"><span data-stu-id="db2ab-104"><<<<<<< HEAD Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="db2ab-105">Dans ce scénario, ADO, le fournisseur de la base de données OLE sous-jacent qu'il utilise, ainsi que tous les autres composants requis pour référencer un magasin de données particulier sont installés sur un serveur exécutant IIS (Internet Information Services).</span><span class="sxs-lookup"><span data-stu-id="db2ab-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="db2ab-106">Avec ASP (Active Server Pages), ADO est un composant référencé dans un script qui peut générer, par exemple, du contenu HTML.</span><span class="sxs-lookup"><span data-stu-id="db2ab-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="db2ab-107">Ce contenu peut être transmis, via HTTP, à un navigateur Web client.</span><span class="sxs-lookup"><span data-stu-id="db2ab-107">This HTML content can be passed via HTTP to a client Web browser.</span></span> <span data-ttu-id="db2ab-108">L'environnement de script permet à la page Web de renvoyer des actions au script côté serveur et ainsi, de mettre à jour, de traverser ou de consulter des données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="db2ab-108">Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
<span data-ttu-id="db2ab-109">=== Dans un environnement de script, ADO permet d’exposer des données via les scripts côté serveur.</span><span class="sxs-lookup"><span data-stu-id="db2ab-109">======= Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="db2ab-110">Dans ce scénario, ADO, le fournisseur de la base de données OLE sous-jacent qu'il utilise, ainsi que tous les autres composants requis pour référencer un magasin de données particulier sont installés sur un serveur exécutant IIS (Internet Information Services).</span><span class="sxs-lookup"><span data-stu-id="db2ab-110">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="db2ab-111">Avec ASP (Active Server Pages), ADO est un composant référencé dans un script qui peut générer, par exemple, du contenu HTML.</span><span class="sxs-lookup"><span data-stu-id="db2ab-111">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="db2ab-112">Ce contenu HTML peut être transmis via le protocole HTTP pour un navigateur web client.</span><span class="sxs-lookup"><span data-stu-id="db2ab-112">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="db2ab-113">Grâce à l’utilisation d’un script, la page Web peut renvoyer des actions au script côté serveur, ce qui vous permet de mettre à jour, de traverser ou afficher des données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="db2ab-113">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>
>>>>>>> <span data-ttu-id="db2ab-114">master</span><span class="sxs-lookup"><span data-stu-id="db2ab-114">master</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="db2ab-115">Sources de données ODBC</span><span class="sxs-lookup"><span data-stu-id="db2ab-115">ODBC Data Sources</span></span>

<span data-ttu-id="db2ab-p102">La source de données ODBC, lorsqu'elle est utilisée, constitue une différence notable entre les codes ADO avec et sans script. Dans les applications sans script, vous pouvez créer un DSN utilisateur dans l'administrateur de la source de données ODBC. Pour les scripts exécutés sous IIS, vous devez créer un DSN système, sans quoi, vos scripts ne reconnaîtront pas la source de données que vous avez créée. Ceci vaut pour toutes les applications de script ADO qui utilisent le fournisseur de base de données Microsoft OLE pour la source de données ODBC via Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="db2ab-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="db2ab-120">Référence à la bibliothèque ADO</span><span class="sxs-lookup"><span data-stu-id="db2ab-120">Referencing the ADO Library</span></span>

<span data-ttu-id="db2ab-121">N/A avec des langages de script</span><span class="sxs-lookup"><span data-stu-id="db2ab-121">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="db2ab-122">Gestion d'événements</span><span class="sxs-lookup"><span data-stu-id="db2ab-122">Handling events</span></span>

<span data-ttu-id="db2ab-123">N/A avec des langages de script</span><span class="sxs-lookup"><span data-stu-id="db2ab-123">N/A with scripting languages.</span></span>

<span data-ttu-id="db2ab-124">Les rubriques suivantes contiennent des informations détaillées sur l'utilisation d'ADO avec des langages de script :</span><span class="sxs-lookup"><span data-stu-id="db2ab-124">The following topics contain more specific information about using ADO with scripting languages:</span></span>

  - [<span data-ttu-id="db2ab-125">Programmation ADO en VBScript</span><span class="sxs-lookup"><span data-stu-id="db2ab-125">ADO in VBScript</span></span>](vbscript-ado-programming.md)

  - [<span data-ttu-id="db2ab-126">Programmation ADO en Jscript</span><span class="sxs-lookup"><span data-stu-id="db2ab-126">ADO in JScript</span></span>](jscript-ado-programming.md)


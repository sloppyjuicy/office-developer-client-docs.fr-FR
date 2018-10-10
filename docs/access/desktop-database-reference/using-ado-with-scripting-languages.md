---
title: Utilisation d'ADO avec des langages de script
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2de5cd9507ede3308a207b078a5bc66a4917e267
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472419"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="0095b-102">Utilisation d'ADO avec des langages de script</span><span class="sxs-lookup"><span data-stu-id="0095b-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="0095b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0095b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0095b-p101">Dans un environnement de script, ADO vous permet d'exposer des données via un script côté serveur. Dans ce scénario, ADO, le fournisseur de la base de données OLE sous-jacent qu'il utilise, ainsi que tous les autres composants requis pour référencer un magasin de données particulier sont installés sur un serveur exécutant IIS (Internet Information Services). Avec ASP (Active Server Pages), ADO est un composant référencé dans un script qui peut générer, par exemple, du contenu HTML. Ce contenu peut être transmis, via HTTP, à un navigateur Web client. L'environnement de script permet à la page Web de renvoyer des actions au script côté serveur et ainsi, de mettre à jour, de traverser ou de consulter des données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0095b-p101">Within a scripting environment, ADO allows you to expose data by way of server-side scripting. In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS). Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example. This HTML content can be passed via HTTP to a client Web browser. Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="0095b-109">Sources de données ODBC</span><span class="sxs-lookup"><span data-stu-id="0095b-109">ODBC Data Sources</span></span>

<span data-ttu-id="0095b-p102">La source de données ODBC, lorsqu'elle est utilisée, constitue une différence notable entre les codes ADO avec et sans script. Dans les applications sans script, vous pouvez créer un DSN utilisateur dans l'administrateur de la source de données ODBC. Pour les scripts exécutés sous IIS, vous devez créer un DSN système, sans quoi, vos scripts ne reconnaîtront pas la source de données que vous avez créée. Ceci vaut pour toutes les applications de script ADO qui utilisent le fournisseur de base de données Microsoft OLE pour la source de données ODBC via Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="0095b-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="0095b-114">Référence à la bibliothèque ADO</span><span class="sxs-lookup"><span data-stu-id="0095b-114">Referencing the ADO Library</span></span>

<span data-ttu-id="0095b-115">N/A avec des langages de script</span><span class="sxs-lookup"><span data-stu-id="0095b-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="0095b-116">Gestion d'événements</span><span class="sxs-lookup"><span data-stu-id="0095b-116">Handling events</span></span>

<span data-ttu-id="0095b-117">N/A avec des langages de script</span><span class="sxs-lookup"><span data-stu-id="0095b-117">N/A with scripting languages.</span></span>

<span data-ttu-id="0095b-118">Les rubriques suivantes contiennent des informations détaillées sur l'utilisation d'ADO avec des langages de script :</span><span class="sxs-lookup"><span data-stu-id="0095b-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

  - [<span data-ttu-id="0095b-119">Programmation ADO en VBScript</span><span class="sxs-lookup"><span data-stu-id="0095b-119">ADO in VBScript</span></span>](vbscript-ado-programming.md)

  - [<span data-ttu-id="0095b-120">Programmation ADO en Jscript</span><span class="sxs-lookup"><span data-stu-id="0095b-120">ADO in JScript</span></span>](jscript-ado-programming.md)


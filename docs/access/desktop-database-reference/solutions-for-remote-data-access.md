---
title: Solutions pour l'accès à distance aux données
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c03a6495b6d95723469d14dc1c3d9d2972760865
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937168"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="b4827-102">Solutions pour l'accès à distance aux données</span><span class="sxs-lookup"><span data-stu-id="b4827-102">Solutions for Remote Data Access</span></span>


<span data-ttu-id="b4827-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4827-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="b4827-104">Le problème</span><span class="sxs-lookup"><span data-stu-id="b4827-104">The Issue</span></span>

<span data-ttu-id="b4827-p101">ADO permet à votre application d'accéder directement aux sources de données et de les modifier (système à deux couches). Par exemple, si vous êtes connecté à la source de données qui contient vos données, il s'agit d'une connexion directe dans un système à deux couches.</span><span class="sxs-lookup"><span data-stu-id="b4827-p101">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system). For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="b4827-107">Toutefois, vous souhaiterez peut-être accéder aux sources de données indirectement via un intermédiaire tel que Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="b4827-107">However, you may want to access data sources indirectly through an intermediary such as Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="b4827-108">Ce type de système est parfois appelé système à trois couches.</span><span class="sxs-lookup"><span data-stu-id="b4827-108">This arrangement is sometimes called a three-tier system.</span></span> <span data-ttu-id="b4827-109">IIS est un système client/serveur qui fournit à une application locale ou cliente un moyen efficace d'appeler un programme distant (serveur) sur Internet ou dans un intranet.</span><span class="sxs-lookup"><span data-stu-id="b4827-109">IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</span></span> <span data-ttu-id="b4827-110">Le programme serveur accède à la source des données et traite éventuellement les données acquises.</span><span class="sxs-lookup"><span data-stu-id="b4827-110">The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="b4827-111">Par exemple, votre page Web intranet contient une application écrite en Microsoft Visual Basic Scripting Edition (VBScript), qui se connecte à IIS.</span><span class="sxs-lookup"><span data-stu-id="b4827-111">For example, your intranet webpage contains an application written in Microsoft Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="b4827-112">IIS se connecte à son tour à la source de données, extrait les données et les traite d'une façon quelconque, puis retourne les informations traitées à votre application.</span><span class="sxs-lookup"><span data-stu-id="b4827-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>

<span data-ttu-id="b4827-p104">Dans cet exemple, votre application ne se connecte jamais directement à la source de données ; c'est IIS qui s'y connecte et accède aux données par l'intermédiaire d'ADO.</span><span class="sxs-lookup"><span data-stu-id="b4827-p104">In this example, your application never directly connected to the data source; IIS did. And IIS accessed the data by means of ADO.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b4827-p105">[!REMARQUE] L'application client/serveur ne doit pas nécessairement être basée sur Internet ou un intranet (application de type Web) ; elle peut se composer uniquement des programmes compilés sur un réseau local. Cependant, il s'agit généralement d'une application de type Web.</span><span class="sxs-lookup"><span data-stu-id="b4827-p105">The client/server application does not have to be based on the Internet or an intranet (that is, Web-based) — it could consist solely of compiled programs on a local area network. However, the typical case is a Web-based application.</span></span></P>



<span data-ttu-id="b4827-117">Dans la mesure où certains contrôles visuels, tels que les grilles, les cases à cocher ou les listes, sont susceptibles d'utiliser les informations retournées, ils doivent être en mesure de les manipuler facilement.</span><span class="sxs-lookup"><span data-stu-id="b4827-117">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="b4827-p106">Si vous voulez une interface de programmation d'application simple et efficace, capable de prendre en charge les systèmes à trois couches et de renvoyer les informations comme si elles avaient été extraites d'un système à deux couches, l'interface RDS (Remote Data Service) est l'interface qu'il vous faut.</span><span class="sxs-lookup"><span data-stu-id="b4827-p106">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system. Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="b4827-120">La solution</span><span class="sxs-lookup"><span data-stu-id="b4827-120">The Solution</span></span>

<span data-ttu-id="b4827-p107">RDS définit un modèle de programmation, à savoir la séquence d'activités requise pour accéder à la source de données et la mettre à jour, qui permet d'accéder aux données via un intermédiaire, par exemple Internet Information Services (IIS). Le modèle de programmation résume toutes les fonctionnalités de l'interface RDS.</span><span class="sxs-lookup"><span data-stu-id="b4827-p107">RDS defines a programming model — the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS). The programming model summarizes the entire functionality of RDS.</span></span>


---
title: Utilisation de RDS avec le regroupement de connexions ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87d380fdc52cdee2aa834fd6e78ff1b761a0e93a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312116"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="f57cd-102">Utilisation RDS avec le regroupement de connexion ODBC</span><span class="sxs-lookup"><span data-stu-id="f57cd-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="f57cd-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f57cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f57cd-p101">Si vous utilisez une source de données ODBC, vous pouvez utiliser l'option de regroupement de connexions IIS (Internet Information Services) pour bénéficier d'une gestion haute performance de la charge client. Le regroupement de connexions est un gestionnaire de ressources pour les connexions, qui maintient l'état ouvert sur les connexions fréquemment utilisées.</span><span class="sxs-lookup"><span data-stu-id="f57cd-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="f57cd-106">Pour activer le regroupement de connexions, reportez-vous à la documentation IIS.</span><span class="sxs-lookup"><span data-stu-id="f57cd-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="f57cd-107">Notez que l’activation de la mise en pool de connexions peut soumettre le serveur web à d’autres restrictions, comme indiqué dans la documentation Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="f57cd-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="f57cd-108">Pour assurer la stabilité du regroupement de connexions et bénéficier de performances optimales, vous devez configurer Microsoft SQL Server afin qu'il utilise la bibliothèque réseau de sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f57cd-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="f57cd-109">Pour ce faire, vous devez :</span><span class="sxs-lookup"><span data-stu-id="f57cd-109">To do this, you need to:</span></span>

  - <span data-ttu-id="f57cd-110">configurer l'ordinateur SQL Server pour une utilisation des sockets TCP/IP ;</span><span class="sxs-lookup"><span data-stu-id="f57cd-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="f57cd-111">Configurez le serveur web pour utiliser les sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f57cd-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="f57cd-112">Configuration de l'ordinateur SQL Server pour une utilisation des sockets TCP/IP</span><span class="sxs-lookup"><span data-stu-id="f57cd-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="f57cd-113">Sur l'ordinateur SQL Server, exécutez le programme d'installation de SQL Server de sorte que la bibliothèque réseau de sockets TCP/IP soit utilisée lors des interactions avec la source de données.</span><span class="sxs-lookup"><span data-stu-id="f57cd-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="f57cd-114">**Pour spécifier la bibliothèque réseau de sockets TCP/IP sur l'ordinateur SQL Server**</span><span class="sxs-lookup"><span data-stu-id="f57cd-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="f57cd-115">**Dans Microsoft SQL Server 6.5 :**</span><span class="sxs-lookup"><span data-stu-id="f57cd-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="f57cd-116">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Installation de SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="f57cd-117">Cliquez deux fois sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="f57cd-118">Dans la boîte de dialogue **Microsoft SQL Server  Options**, sélectionnez **Modifier la prise en charge du réseau**, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="f57cd-119">Assurez-vous que la case à cocher **Sockets TCP/IP** est activée, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="f57cd-120">Cliquez sur **Continuer** pour terminer et quitter le programme d'installation.</span><span class="sxs-lookup"><span data-stu-id="f57cd-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="f57cd-121">**Dans Microsoft SQL Server 7.0 :**</span><span class="sxs-lookup"><span data-stu-id="f57cd-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="f57cd-122">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire Réseau Serveur**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="f57cd-123">Sous l'onglet **Général** de la boîte de dialogue, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="f57cd-124">Dans la boîte de dialogue **Ajouter une configuration de bibliothèque réseau**, cliquez sur **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="f57cd-125">Dans les zones **Numéro de port** et **Adresse Proxy**, entrez le numéro de port et l'adresse proxy fournis par votre administrateur réseau.</span><span class="sxs-lookup"><span data-stu-id="f57cd-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="f57cd-126">Cliquez sur **OK** pour terminer et quitter le programme d'installation.</span><span class="sxs-lookup"><span data-stu-id="f57cd-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="f57cd-127">Configuration du serveur web pour utiliser les sockets TCP/IP</span><span class="sxs-lookup"><span data-stu-id="f57cd-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="f57cd-128">Deux options s’offrent à vous pour configurer le serveur web afin qu’il utilise des sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f57cd-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="f57cd-129">Ce que vous faites varie selon que tous les serveurs SQL sont accessibles à partir du serveur web ou que seule une SQL Server spécifique est accessible à partir du serveur web.</span><span class="sxs-lookup"><span data-stu-id="f57cd-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="f57cd-130">Si tous les SQL sont accessibles à partir du serveur web, vous devez exécuter l’utilitaire de configuration du client SQL Server sur l’ordinateur serveur web.</span><span class="sxs-lookup"><span data-stu-id="f57cd-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="f57cd-131">Les étapes suivantes modifient la bibliothèque réseau par défaut pour toutes les connexions SQL Server de ce serveur web IIS afin d’utiliser la bibliothèque réseau de sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f57cd-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="f57cd-132">**Pour configurer le serveur web (tous les serveurs SQL)**</span><span class="sxs-lookup"><span data-stu-id="f57cd-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="f57cd-133">**Pour Microsoft SQL Server 6.5 :**</span><span class="sxs-lookup"><span data-stu-id="f57cd-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="f57cd-134">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Utilitaire de configuration de client SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="f57cd-135">Cliquez sur l'onglet **Net-Library**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="f57cd-136">Dans la zone **Réseau par défaut**, sélectionnez **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="f57cd-137">Cliquez sur **Terminé** pour enregistrer les modifications et quitter l'utilitaire.</span><span class="sxs-lookup"><span data-stu-id="f57cd-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="f57cd-138">**Pour Microsoft SQL Server 7.0 :**</span><span class="sxs-lookup"><span data-stu-id="f57cd-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="f57cd-139">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire Réseau Client**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="f57cd-140">Cliquez sur l'onglet **Général**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="f57cd-141">Dans la zone **Bibliothèque réseau par défaut**, cliquez sur **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="f57cd-142">Cliquez sur **OK** pour enregistrer les modifications et quitter l'utilitaire.</span><span class="sxs-lookup"><span data-stu-id="f57cd-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="f57cd-143">Si une SQL Server spécifique est accessible à partir d’un serveur web, vous devez exécuter l’utilitaire de configuration du client SQL Server sur l’ordinateur serveur web.</span><span class="sxs-lookup"><span data-stu-id="f57cd-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="f57cd-144">Pour modifier la bibliothèque réseau pour une connexion SQL Server spécifique, configurez le logiciel SQL Server client sur l’ordinateur serveur web comme suit.</span><span class="sxs-lookup"><span data-stu-id="f57cd-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="f57cd-145">**Pour configurer le serveur web (une SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="f57cd-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="f57cd-146">**Pour Microsoft SQL Server 6.5 :**</span><span class="sxs-lookup"><span data-stu-id="f57cd-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="f57cd-147">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Utilitaire de configuration de client SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="f57cd-148">Cliquez sur l'onglet **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="f57cd-149">Dans la zone **Serveur**, tapez le nom du serveur auquel se connecter à l'aide de **sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="f57cd-150">Dans la zone **Nom de DLL**, sélectionnez **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="f57cd-p105">Cliquez sur **Ajouter/Modifier**. Toutes les sources de données pointant vers ce serveur utiliseront désormais les sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f57cd-p105">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="f57cd-153">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-153">Click **Done**.</span></span>

<span data-ttu-id="f57cd-154">**Pour Microsoft SQL Server 7.0 :**</span><span class="sxs-lookup"><span data-stu-id="f57cd-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="f57cd-155">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire de configuration de client**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="f57cd-156">Cliquez sur l'onglet **Général**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="f57cd-157">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f57cd-157">Click **Add**.</span></span>

4.  <span data-ttu-id="f57cd-p106">Entrez l'alias du serveur dans la zone **Alias du serveur**. Dans la zone **Bibliothèques réseau**, cliquez sur **TCP/IP**. Dans la zone **Nom de l'ordinateur**, entrez le nom de l'ordinateur qui est à l'écoute des clients utilisant des sockets TCP/IP. Dans la zone **Numéro de port**, entrez le port d'écoute utilisé par le serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f57cd-p106">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="f57cd-162">Click **OK**, and then **OK** again to exit the utility.</span><span class="sxs-lookup"><span data-stu-id="f57cd-162">Click **OK**, and then **OK** again to exit the utility.</span></span>


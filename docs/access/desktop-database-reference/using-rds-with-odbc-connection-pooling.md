---
title: Utilisation de RDS avec le regroupement de connexions ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7baaf81d7a5d6a91416ea5baf8ba57745612740e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469436"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="16004-102">Utilisation de RDS avec le regroupement de connexions ODBC</span><span class="sxs-lookup"><span data-stu-id="16004-102">Using RDS with ODBC Connection Pooling</span></span>


<span data-ttu-id="16004-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="16004-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="16004-p101">Si vous utilisez une source de données ODBC, vous pouvez utiliser l'option de regroupement de connexions IIS (Internet Information Services) pour bénéficier d'une gestion haute performance de la charge client. Le regroupement de connexions est un gestionnaire de ressources pour les connexions, qui maintient l'état ouvert sur les connexions fréquemment utilisées.</span><span class="sxs-lookup"><span data-stu-id="16004-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="16004-106">Pour activer le regroupement de connexions, reportez-vous à la documentation IIS.</span><span class="sxs-lookup"><span data-stu-id="16004-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="16004-107">Il est à noter que l'activation du regroupement de connexions est susceptible d'imposer au serveur Web d'autres restrictions, comme le mentionne la documentation Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="16004-107">Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="16004-108">Pour assurer la stabilité du regroupement de connexions et bénéficier de performances optimales, vous devez configurer Microsoft SQL Server afin qu'il utilise la bibliothèque réseau de sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="16004-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="16004-109">Pour ce faire, vous devez :</span><span class="sxs-lookup"><span data-stu-id="16004-109">To do this, you need to:</span></span>

  - <span data-ttu-id="16004-110">configurer l'ordinateur SQL Server pour une utilisation des sockets TCP/IP ;</span><span class="sxs-lookup"><span data-stu-id="16004-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="16004-111">configurer le serveur Web pour une utilisation des sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="16004-111">Configure the Web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="16004-112">Configuration de l'ordinateur SQL Server pour une utilisation des sockets TCP/IP</span><span class="sxs-lookup"><span data-stu-id="16004-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="16004-113">Sur l'ordinateur SQL Server, exécutez le programme d'installation de SQL Server de sorte que la bibliothèque réseau de sockets TCP/IP soit utilisée lors des interactions avec la source de données.</span><span class="sxs-lookup"><span data-stu-id="16004-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="16004-114">**Pour spécifier la bibliothèque réseau de sockets TCP/IP sur l'ordinateur SQL Server**</span><span class="sxs-lookup"><span data-stu-id="16004-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="16004-115">**Dans Microsoft SQL Server 6.5 :**</span><span class="sxs-lookup"><span data-stu-id="16004-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="16004-116">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Installation de SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="16004-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="16004-117">Cliquez deux fois sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="16004-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="16004-118">Dans la boîte de dialogue **Microsoft SQL Server  Options**, sélectionnez **Modifier la prise en charge du réseau**, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="16004-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="16004-119">Assurez-vous que la case à cocher **Sockets TCP/IP** est activée, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="16004-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="16004-120">Cliquez sur **Continuer** pour terminer et quitter le programme d'installation.</span><span class="sxs-lookup"><span data-stu-id="16004-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="16004-121">**Dans Microsoft SQL Server 7.0 :**</span><span class="sxs-lookup"><span data-stu-id="16004-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="16004-122">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire Réseau Serveur**.</span><span class="sxs-lookup"><span data-stu-id="16004-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="16004-123">Sous l'onglet **Général** de la boîte de dialogue, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="16004-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="16004-124">Dans la boîte de dialogue **Ajouter une configuration de bibliothèque réseau**, cliquez sur **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="16004-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="16004-125">Dans les zones **Numéro de port** et **Adresse Proxy**, entrez le numéro de port et l'adresse proxy fournis par votre administrateur réseau.</span><span class="sxs-lookup"><span data-stu-id="16004-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="16004-126">Cliquez sur **OK** pour terminer et quitter le programme d'installation.</span><span class="sxs-lookup"><span data-stu-id="16004-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="16004-127">Configuration du serveur Web pour une utilisation des sockets TCP/IP</span><span class="sxs-lookup"><span data-stu-id="16004-127">Configuring the Web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="16004-p102">Pour configurer le serveur Web en vue d'une utilisation des sockets TCP/IP, vous devez utiliser l'une ou l'autre des deux options disponibles, selon que l'accès à tous les serveurs SQL Server s'effectue à partir du serveur Web, ou que ce dernier n'accède qu'à un seul serveur SQL Server spécifique.</span><span class="sxs-lookup"><span data-stu-id="16004-p102">There are two options for configuring the Web server to use TCP/IP Sockets. What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</span></span>

<span data-ttu-id="16004-p103">Si l'accès à tous les serveurs SQL Server s'effectue à partir du serveur Web, vous devez exécuter l'utilitaire de configuration de client SQL Server sur le serveur Web. La procédure suivante modifie la bibliothèque réseau par défaut pour toutes les connexions SQL Server établies à partir de ce serveur Web IIS en vue de l'utilisation de la bibliothèque réseau de sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="16004-p103">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="16004-132">**Pour configurer le serveur Web (tous les serveurs SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="16004-132">**To configure the Web server (all SQL Servers)**</span></span>

<span data-ttu-id="16004-133">**Pour Microsoft SQL Server 6.5 :**</span><span class="sxs-lookup"><span data-stu-id="16004-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="16004-134">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Utilitaire de configuration de client SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="16004-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="16004-135">Cliquez sur l'onglet **Net-Library**.</span><span class="sxs-lookup"><span data-stu-id="16004-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="16004-136">Dans la zone **Réseau par défaut**, sélectionnez **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="16004-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="16004-137">Cliquez sur **Terminé** pour enregistrer les modifications et quitter l'utilitaire.</span><span class="sxs-lookup"><span data-stu-id="16004-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="16004-138">**Pour Microsoft SQL Server 7.0 :**</span><span class="sxs-lookup"><span data-stu-id="16004-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="16004-139">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire Réseau Client**.</span><span class="sxs-lookup"><span data-stu-id="16004-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="16004-140">Cliquez sur l'onglet **Général**.</span><span class="sxs-lookup"><span data-stu-id="16004-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="16004-141">Dans la zone **Bibliothèque réseau par défaut**, cliquez sur **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="16004-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="16004-142">Cliquez sur **OK** pour enregistrer les modifications et quitter l'utilitaire.</span><span class="sxs-lookup"><span data-stu-id="16004-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="16004-p104">Si l'accès à un serveur SQL Server spécifique s'effectue à partir d'un serveur Web, vous devez exécuter l'utilitaire de configuration de client SQL Server sur le serveur Web. Pour modifier la bibliothèque réseau pour une connexion SQL Server spécifique, configurez le logiciel Client SQL Server sur le serveur Web comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="16004-p104">If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</span></span>

<span data-ttu-id="16004-145">**Pour configurer le serveur Web (serveur SQL Server spécifique)**</span><span class="sxs-lookup"><span data-stu-id="16004-145">**To configure the Web server (a specific SQL Server)**</span></span>

<span data-ttu-id="16004-146">**Pour Microsoft SQL Server 6.5 :**</span><span class="sxs-lookup"><span data-stu-id="16004-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="16004-147">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Utilitaire de configuration de client SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="16004-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="16004-148">Cliquez sur l'onglet **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="16004-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="16004-149">Dans la zone **Serveur**, tapez le nom du serveur auquel se connecter à l'aide de **sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="16004-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="16004-150">Dans la zone **Nom de DLL**, sélectionnez **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="16004-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="16004-p105">Cliquez sur **Ajouter/Modifier**. Toutes les sources de données pointant vers ce serveur utiliseront désormais les sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="16004-p105">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="16004-153">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="16004-153">Click **Done**.</span></span>

<span data-ttu-id="16004-154">**Pour Microsoft SQL Server 7.0 :**</span><span class="sxs-lookup"><span data-stu-id="16004-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="16004-155">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire de configuration de client**.</span><span class="sxs-lookup"><span data-stu-id="16004-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="16004-156">Cliquez sur l'onglet **Général**.</span><span class="sxs-lookup"><span data-stu-id="16004-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="16004-157">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="16004-157">Click **Add**.</span></span>

4.  <span data-ttu-id="16004-p106">Entrez l'alias du serveur dans la zone **Alias du serveur**. Dans la zone **Bibliothèques réseau**, cliquez sur **TCP/IP**. Dans la zone **Nom de l'ordinateur**, entrez le nom de l'ordinateur qui est à l'écoute des clients utilisant des sockets TCP/IP. Dans la zone **Numéro de port**, entrez le port d'écoute utilisé par le serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="16004-p106">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="16004-162">Cliquez sur **OK**, puis sur **OK** à nouveau pour quitter l’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="16004-162">Click **OK**, and then **OK** again to exit the utility.</span></span>


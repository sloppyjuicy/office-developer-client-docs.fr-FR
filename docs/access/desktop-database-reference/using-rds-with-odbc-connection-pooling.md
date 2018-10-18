---
title: Utilisation de RDS avec le regroupement de connexions ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee66e68cb8eeaaca57c007dc64a9e2b3a8476ec7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606016"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="d8e83-102">Utilisation de RDS avec le regroupement de connexions ODBC</span><span class="sxs-lookup"><span data-stu-id="d8e83-102">Using RDS with ODBC Connection Pooling</span></span>


<span data-ttu-id="d8e83-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8e83-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d8e83-p101">Si vous utilisez une source de données ODBC, vous pouvez utiliser l'option de regroupement de connexions IIS (Internet Information Services) pour bénéficier d'une gestion haute performance de la charge client. Le regroupement de connexions est un gestionnaire de ressources pour les connexions, qui maintient l'état ouvert sur les connexions fréquemment utilisées.</span><span class="sxs-lookup"><span data-stu-id="d8e83-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="d8e83-106">Pour activer le regroupement de connexions, reportez-vous à la documentation IIS.</span><span class="sxs-lookup"><span data-stu-id="d8e83-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="d8e83-107"><<<<<<< Tête Remarque que l’activation de regroupement de connexions peut-être imposer au serveur Web d’autres restrictions, comme indiqué dans la documentation de Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="d8e83-107"><<<<<<< HEAD Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
<span data-ttu-id="d8e83-108">=== Veuillez noter que l’activation du regroupement connexion peut-être imposer au serveur web d’autres restrictions, comme indiqué dans la documentation de Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="d8e83-108">======= Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
>>>>>>> <span data-ttu-id="d8e83-109">master</span><span class="sxs-lookup"><span data-stu-id="d8e83-109">master</span></span>

<span data-ttu-id="d8e83-110">Pour assurer la stabilité du regroupement de connexions et bénéficier de performances optimales, vous devez configurer Microsoft SQL Server afin qu'il utilise la bibliothèque réseau de sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d8e83-110">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="d8e83-111">Pour ce faire, vous devez :</span><span class="sxs-lookup"><span data-stu-id="d8e83-111">To do this, you need to:</span></span>

  - <span data-ttu-id="d8e83-112">configurer l'ordinateur SQL Server pour une utilisation des sockets TCP/IP ;</span><span class="sxs-lookup"><span data-stu-id="d8e83-112">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

<span data-ttu-id="d8e83-113"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="d8e83-113"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="d8e83-114">configurer le serveur Web pour une utilisation des sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d8e83-114">Configure the Web server to use TCP/IP Sockets.</span></span>
=======
  - <span data-ttu-id="d8e83-115">Configurer le serveur web pour une utilisation des Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d8e83-115">Configure the web server to use TCP/IP Sockets.</span></span>
>>>>>>> <span data-ttu-id="d8e83-116">master</span><span class="sxs-lookup"><span data-stu-id="d8e83-116">master</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="d8e83-117">Configuration de l'ordinateur SQL Server pour une utilisation des sockets TCP/IP</span><span class="sxs-lookup"><span data-stu-id="d8e83-117">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="d8e83-118">Sur l'ordinateur SQL Server, exécutez le programme d'installation de SQL Server de sorte que la bibliothèque réseau de sockets TCP/IP soit utilisée lors des interactions avec la source de données.</span><span class="sxs-lookup"><span data-stu-id="d8e83-118">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="d8e83-119">**Pour spécifier la bibliothèque réseau de sockets TCP/IP sur l'ordinateur SQL Server**</span><span class="sxs-lookup"><span data-stu-id="d8e83-119">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="d8e83-120">**Dans Microsoft SQL Server 6.5 :**</span><span class="sxs-lookup"><span data-stu-id="d8e83-120">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="d8e83-121">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Installation de SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-121">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="d8e83-122">Cliquez deux fois sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-122">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="d8e83-123">Dans la boîte de dialogue **Microsoft SQL Server  Options**, sélectionnez **Modifier la prise en charge du réseau**, puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-123">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="d8e83-124">Assurez-vous que la case à cocher **Sockets TCP/IP** est activée, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-124">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="d8e83-125">Cliquez sur **Continuer** pour terminer et quitter le programme d'installation.</span><span class="sxs-lookup"><span data-stu-id="d8e83-125">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="d8e83-126">**Dans Microsoft SQL Server 7.0 :**</span><span class="sxs-lookup"><span data-stu-id="d8e83-126">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="d8e83-127">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire Réseau Serveur**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-127">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="d8e83-128">Sous l'onglet **Général** de la boîte de dialogue, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-128">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="d8e83-129">Dans la boîte de dialogue **Ajouter une configuration de bibliothèque réseau**, cliquez sur **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-129">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="d8e83-130">Dans les zones **Numéro de port** et **Adresse Proxy**, entrez le numéro de port et l'adresse proxy fournis par votre administrateur réseau.</span><span class="sxs-lookup"><span data-stu-id="d8e83-130">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="d8e83-131">Cliquez sur **OK** pour terminer et quitter le programme d'installation.</span><span class="sxs-lookup"><span data-stu-id="d8e83-131">Click **OK** to finish, and exit setup.</span></span>

<span data-ttu-id="d8e83-132"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="d8e83-132"><<<<<<< HEAD</span></span>
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="d8e83-133">Configuration du serveur Web pour une utilisation des sockets TCP/IP</span><span class="sxs-lookup"><span data-stu-id="d8e83-133">Configuring the Web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="d8e83-p103">Pour configurer le serveur Web en vue d'une utilisation des sockets TCP/IP, vous devez utiliser l'une ou l'autre des deux options disponibles, selon que l'accès à tous les serveurs SQL Server s'effectue à partir du serveur Web, ou que ce dernier n'accède qu'à un seul serveur SQL Server spécifique.</span><span class="sxs-lookup"><span data-stu-id="d8e83-p103">There are two options for configuring the Web server to use TCP/IP Sockets. What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</span></span>

<span data-ttu-id="d8e83-p104">Si l'accès à tous les serveurs SQL Server s'effectue à partir du serveur Web, vous devez exécuter l'utilitaire de configuration de client SQL Server sur le serveur Web. La procédure suivante modifie la bibliothèque réseau par défaut pour toutes les connexions SQL Server établies à partir de ce serveur Web IIS en vue de l'utilisation de la bibliothèque réseau de sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d8e83-p104">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</span></span>

<a name="to-configure-the-web-server-all-sql-servers"></a><span data-ttu-id="d8e83-138">**Pour configurer le serveur Web (tous les serveurs SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="d8e83-138">**To configure the Web server (all SQL Servers)**</span></span>
=======
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="d8e83-139">Configuration du serveur pour l’utilisation des Sockets TCP/IP web</span><span class="sxs-lookup"><span data-stu-id="d8e83-139">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="d8e83-140">Il existe deux options de configuration du serveur web pour utiliser des Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d8e83-140">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="d8e83-141">Que faire dépend si tous les serveurs SQL sont accessibles à partir du serveur web, ou uniquement un serveur SQL Server spécifique est accessible à partir du serveur web.</span><span class="sxs-lookup"><span data-stu-id="d8e83-141">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="d8e83-142">Si tous les serveurs SQL sont accessibles à partir du serveur web, vous devez exécuter l’utilitaire de Configuration de Client SQL Server sur l’ordinateur serveur web.</span><span class="sxs-lookup"><span data-stu-id="d8e83-142">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="d8e83-143">La procédure suivante modifie la bibliothèque réseau par défaut pour toutes les connexions SQL Server sont effectuées à partir de ce serveur web IIS à utiliser la bibliothèque réseau de Sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d8e83-143">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="d8e83-144">**Pour configurer le serveur web (tous les serveurs SQL)**</span><span class="sxs-lookup"><span data-stu-id="d8e83-144">**To configure the web server (all SQL Servers)**</span></span>
>>>>>>> <span data-ttu-id="d8e83-145">master</span><span class="sxs-lookup"><span data-stu-id="d8e83-145">master</span></span>

<span data-ttu-id="d8e83-146">**Pour Microsoft SQL Server 6.5 :**</span><span class="sxs-lookup"><span data-stu-id="d8e83-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="d8e83-147">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Utilitaire de configuration de client SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="d8e83-148">Cliquez sur l'onglet **Net-Library**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-148">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="d8e83-149">Dans la zone **Réseau par défaut**, sélectionnez **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-149">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="d8e83-150">Cliquez sur **Terminé** pour enregistrer les modifications et quitter l'utilitaire.</span><span class="sxs-lookup"><span data-stu-id="d8e83-150">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="d8e83-151">**Pour Microsoft SQL Server 7.0 :**</span><span class="sxs-lookup"><span data-stu-id="d8e83-151">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="d8e83-152">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire Réseau Client**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-152">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="d8e83-153">Cliquez sur l'onglet **Général**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-153">Click the **General** tab.</span></span>

3.  <span data-ttu-id="d8e83-154">Dans la zone **Bibliothèque réseau par défaut**, cliquez sur **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-154">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="d8e83-155">Cliquez sur **OK** pour enregistrer les modifications et quitter l'utilitaire.</span><span class="sxs-lookup"><span data-stu-id="d8e83-155">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="d8e83-156"><<<<<<< Tête si SQL Server spécifique est accessible à partir d’un serveur Web, vous devez exécuter l’utilitaire de Configuration de Client SQL Server sur l’ordinateur serveur Web.</span><span class="sxs-lookup"><span data-stu-id="d8e83-156"><<<<<<< HEAD If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</span></span> <span data-ttu-id="d8e83-157">Pour modifier la bibliothèque réseau pour une connexion SQL Server spécifique, configurez le logiciel Client SQL Server sur le serveur Web comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d8e83-157">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</span></span>

<a name="to-configure-the-web-server-a-specific-sql-server"></a><span data-ttu-id="d8e83-158">**Pour configurer le serveur Web (serveur SQL Server spécifique)**</span><span class="sxs-lookup"><span data-stu-id="d8e83-158">**To configure the Web server (a specific SQL Server)**</span></span>
=======
<span data-ttu-id="d8e83-159">Si un serveur SQL Server spécifique est accessible à partir d’un serveur web, vous devez exécuter l’utilitaire de Configuration de Client SQL Server sur l’ordinateur serveur web.</span><span class="sxs-lookup"><span data-stu-id="d8e83-159">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="d8e83-160">Pour modifier la bibliothèque réseau pour une connexion SQL Server spécifique, configurez le logiciel Client de SQL Server sur l’ordinateur serveur web comme suit.</span><span class="sxs-lookup"><span data-stu-id="d8e83-160">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="d8e83-161">**Pour configurer le serveur web (spécifique SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="d8e83-161">**To configure the web server (a specific SQL Server)**</span></span>
>>>>>>> <span data-ttu-id="d8e83-162">master</span><span class="sxs-lookup"><span data-stu-id="d8e83-162">master</span></span>

<span data-ttu-id="d8e83-163">**Pour Microsoft SQL Server 6.5 :**</span><span class="sxs-lookup"><span data-stu-id="d8e83-163">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="d8e83-164">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Utilitaire de configuration de client SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-164">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="d8e83-165">Cliquez sur l'onglet **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-165">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="d8e83-166">Dans la zone **Serveur**, tapez le nom du serveur auquel se connecter à l'aide de **sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-166">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="d8e83-167">Dans la zone **Nom de DLL**, sélectionnez **Sockets TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-167">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="d8e83-p109">Cliquez sur **Ajouter/Modifier**. Toutes les sources de données pointant vers ce serveur utiliseront désormais les sockets TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d8e83-p109">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="d8e83-170">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-170">Click **Done**.</span></span>

<span data-ttu-id="d8e83-171">**Pour Microsoft SQL Server 7.0 :**</span><span class="sxs-lookup"><span data-stu-id="d8e83-171">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="d8e83-172">Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire de configuration de client**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-172">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="d8e83-173">Cliquez sur l'onglet **Général**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-173">Click the **General** tab.</span></span>

3.  <span data-ttu-id="d8e83-174">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d8e83-174">Click **Add**.</span></span>

4.  <span data-ttu-id="d8e83-p110">Entrez l'alias du serveur dans la zone **Alias du serveur**. Dans la zone **Bibliothèques réseau**, cliquez sur **TCP/IP**. Dans la zone **Nom de l'ordinateur**, entrez le nom de l'ordinateur qui est à l'écoute des clients utilisant des sockets TCP/IP. Dans la zone **Numéro de port**, entrez le port d'écoute utilisé par le serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8e83-p110">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="d8e83-179">Cliquez sur **OK**, puis sur **OK** à nouveau pour quitter l’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="d8e83-179">Click **OK**, and then **OK** again to exit the utility.</span></span>


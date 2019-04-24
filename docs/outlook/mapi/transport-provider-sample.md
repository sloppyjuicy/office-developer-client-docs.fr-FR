---
title: Exemple de fournisseur de transport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356587"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="be524-103">Exemple de fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="be524-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="be524-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be524-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be524-105">Cet exemple utilise des fichiers et des répertoires pour transmettre et recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="be524-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="be524-106">Il implémente et enregistre un préprocesseur très simple qui ajoute une ligne de texte à chaque message sortant.</span><span class="sxs-lookup"><span data-stu-id="be524-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="be524-107">L'exemple montre comment fractionner le contenu d'un message entre le format TNEF (Transport Neutral Encapsulation Format) et le texte.</span><span class="sxs-lookup"><span data-stu-id="be524-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="be524-108">Il prend également en charge toutes les options de configuration (feuilles de propriétés, assistants et configuration de la programmation) et les options de message.</span><span class="sxs-lookup"><span data-stu-id="be524-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="be524-109">Il ne prend pas en charge les interfaces de transport à distance.</span><span class="sxs-lookup"><span data-stu-id="be524-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="be524-110">Vous pouvez télécharger cet exemple à partir d' [exemples de code MAPI (Outlook messagING API)](https://go.microsoft.com/fwlink/?LinkId=129740).</span><span class="sxs-lookup"><span data-stu-id="be524-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be524-111">Exécutable</span><span class="sxs-lookup"><span data-stu-id="be524-111">Executable:</span></span>  <br/> |<span data-ttu-id="be524-112">mrxp32. dll</span><span class="sxs-lookup"><span data-stu-id="be524-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="be524-113">Répertoire de code source:</span><span class="sxs-lookup"><span data-stu-id="be524-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="be524-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="be524-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="be524-115">Langue</span><span class="sxs-lookup"><span data-stu-id="be524-115">Language:</span></span>  <br/> |<span data-ttu-id="be524-116">C++</span><span class="sxs-lookup"><span data-stu-id="be524-116">C++</span></span>  <br/> |
|<span data-ttu-id="be524-117">Formes</span><span class="sxs-lookup"><span data-stu-id="be524-117">Platforms:</span></span>  <br/> |<span data-ttu-id="be524-118">Visual Studio 2008 à compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="be524-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="be524-119">Fonctionnalités prises en charge</span><span class="sxs-lookup"><span data-stu-id="be524-119">Supported Features</span></span>

<span data-ttu-id="be524-120">Cet exemple prend en charge les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="be524-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="be524-121">Fonctionnalités de base, telles que l'envoi, la réception et l'interrogation pour les nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="be524-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="be524-122">Configuration interactive et par programmation.</span><span class="sxs-lookup"><span data-stu-id="be524-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="be524-123">Interface **IMAPIStatus** , à l'exception du paramètre Property.</span><span class="sxs-lookup"><span data-stu-id="be524-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="be524-124">Pour plus d'informations, reportez-vous à l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="be524-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="be524-125">Sécurité des threads.</span><span class="sxs-lookup"><span data-stu-id="be524-125">Thread safety.</span></span>
    
- <span data-ttu-id="be524-126">Journalisation des événements dans un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="be524-126">Event logging to a text file.</span></span> <span data-ttu-id="be524-127">Le fichier est automatiquement limité à une taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="be524-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="be524-128">Toutes les sessions de transport utilisent le même fichier.</span><span class="sxs-lookup"><span data-stu-id="be524-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="be524-129">Fonctionnalités non prises en charge</span><span class="sxs-lookup"><span data-stu-id="be524-129">Unsupported Features</span></span>

<span data-ttu-id="be524-130">Cet exemple ne prend pas en charge la détection asynchrone des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="be524-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="be524-131">**Pour installer l'exemple de fournisseur de transport**</span><span class="sxs-lookup"><span data-stu-id="be524-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="be524-132">Pour télécharger l'exemple de fournisseur de transport, consultez [la rubrique téléchargement des exemples MAPI Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="be524-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="be524-133">Recherchez le dossier dans lequel vous avez enregistré les exemples MAPI Outlook.</span><span class="sxs-lookup"><span data-stu-id="be524-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="be524-134">Cliquez avec le bouton droit sur le dossier zip de **\<\> numéro de version OutlookMAPISamples** et cliquez sur **extraire tout**.</span><span class="sxs-lookup"><span data-stu-id="be524-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="be524-135">Cliquez sur **Parcourir**, sélectionnez l'emplacement où vous souhaitez enregistrer l'exemple, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="be524-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="be524-136">Exécutez Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="be524-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="be524-137">Dans Visual Studio 2008, cliquez sur **fichier**, sur **ouvrir**, puis sur **projet/solution**.</span><span class="sxs-lookup"><span data-stu-id="be524-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="be524-138">Naviguez jusqu'à l'emplacement où vous avez enregistré l'exemple, cliquez sur **mrxp32. vcproj**, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="be524-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="be524-139">Dans le menu **générer** , cliquez sur **Gestionnaire de configuration**.</span><span class="sxs-lookup"><span data-stu-id="be524-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="be524-140">Dans la boîte de dialogue **Gestionnaire de configuration** , accédez à la ligne **mrxp32** , puis, dans la colonne **configuration** , sélectionnez **publier**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="be524-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="be524-141">Dans le menu **Générer**, cliquez sur **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="be524-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="be524-142">Dans la boîte de dialogue **enregistrer le fichier sous** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="be524-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="be524-143">Dans le dossier où vous avez enregistré l'exemple, cliquez avec le bouton droit sur le fichier de commandes d'installation, puis cliquez sur **exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="be524-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="be524-144">Dans la boîte de dialogue **contrôle de compte d'utilisateur** , cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="be524-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="be524-145">**install. bat** copie le fichier. dll dans le dossier d'installation par défaut de Microsoft Office, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="be524-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="be524-146">Si vous avez installé les produits Office à un autre emplacement, cliquez avec le bouton droit sur **install. bat** et cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="be524-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="be524-147">Le fichier s'ouvre dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="be524-147">The file opens in Notepad.</span></span> <span data-ttu-id="be524-148">Remplacez le chemin d'installation par défaut par le chemin d'installation utilisé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="be524-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="be524-149">**Pour configurer le fournisseur de transport dans Outlook**</span><span class="sxs-lookup"><span data-stu-id="be524-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="be524-150">Dans le menu **Outils** d'Outlook, cliquez sur **paramètres du compte**.</span><span class="sxs-lookup"><span data-stu-id="be524-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="be524-151">Dans la boîte de dialogue **paramètres du compte** , sous l'onglet **messagerie** , cliquez sur **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="be524-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="be524-152">Sous **choisir le service de messagerie** , cliquez sur **autre**, sélectionnez **MRXP**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be524-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="be524-153">Dans la boîte de dialogue **configuration du transport MRXP** , tapez le **nom complet**de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be524-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="be524-154">Sous **chemin d'accès à la boîte de réception (partage UNC),** entrez un chemin d'accès au dossier.</span><span class="sxs-lookup"><span data-stu-id="be524-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="be524-155">Il peut également s'agir d'un chemin d'accès à un dossier local.</span><span class="sxs-lookup"><span data-stu-id="be524-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="be524-156">Ce chemin d'accès doit exister.</span><span class="sxs-lookup"><span data-stu-id="be524-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="be524-157">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="be524-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="be524-158">Dans la boîte de dialogue **Ajouter un compte de courrier** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="be524-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="be524-159">Cliquez sur **Terminer** , puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="be524-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="be524-160">Pour commencer à utiliser le compte MRXP, quittez et redémarrez Outlook.</span><span class="sxs-lookup"><span data-stu-id="be524-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="be524-161">**Pour utiliser l'exemple de fournisseur de transport pour envoyer un message dans Outlook**</span><span class="sxs-lookup"><span data-stu-id="be524-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="be524-162">Dans le menu **fichier** , cliquez sur **nouveau**, puis sur **message électronique**.</span><span class="sxs-lookup"><span data-stu-id="be524-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="be524-163">Dans la zone **à** , tapez le nom du destinataire au format **[MRXP:\<adresse\>]**.</span><span class="sxs-lookup"><span data-stu-id="be524-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="be524-164">L'adresse est le partage UNC ou le chemin d'accès au dossier local de la boîte de réception du destinataire.</span><span class="sxs-lookup"><span data-stu-id="be524-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="be524-165">S'il y a deux-points ou barres obliques inverses dans l'adresse, vous devez insérer une barre oblique inverse avant chaque signe deux-points ou barre oblique inverse.</span><span class="sxs-lookup"><span data-stu-id="be524-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="be524-166">Par exemple, pour envoyer un message électronique à [MRXP: C: \Mail\myDir], `[MRXP:C\:\\Mail\\myDir]`vous devez taper.</span><span class="sxs-lookup"><span data-stu-id="be524-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="be524-167">L'adresse du destinataire doit exister.</span><span class="sxs-lookup"><span data-stu-id="be524-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="be524-168">Cliquez sur **compte** , puis sur **exemple de transport MRXP**.</span><span class="sxs-lookup"><span data-stu-id="be524-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="be524-169">Tapez votre message, puis cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="be524-169">Type your message and click **Send**.</span></span> <span data-ttu-id="be524-170">Le message est envoyé à l'aide du fournisseur de transport MRXP.</span><span class="sxs-lookup"><span data-stu-id="be524-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="be524-171">**Pour utiliser l'exemple de fournisseur de transport pour recevoir un message dans Outlook**</span><span class="sxs-lookup"><span data-stu-id="be524-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="be524-172">Dans le menu **fichier** , cliquez sur **nouveau**, puis sur **message électronique**.</span><span class="sxs-lookup"><span data-stu-id="be524-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="be524-173">Tapez votre message.</span><span class="sxs-lookup"><span data-stu-id="be524-173">Type your message.</span></span>
    
3. <span data-ttu-id="be524-174">Cliquez sur le **bouton Microsoft Office**, cliquez sur **Enregistrer sous**, puis cliquez sur **Enregistrer sous** pour enregistrer le fichier dans le dossier boîte de réception que vous avez spécifié lors de l'installation.</span><span class="sxs-lookup"><span data-stu-id="be524-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="be524-175">Dans la boîte de dialogue **Enregistrer sous** , accédez au partage UNC ou au dossier local que vous avez défini comme boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="be524-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="be524-176">Dans la liste déroulante **type de fichier** , cliquez sur **format de message Outlook**.</span><span class="sxs-lookup"><span data-stu-id="be524-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="be524-177">Tapez un nom pour le fichier, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="be524-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="be524-178">Le fichier est enregistré dans le dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="be524-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="be524-179">Le fournisseur de transport MRXP remet le message à votre boîte de réception dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="be524-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    


---
title: Exemple de fournisseur de transport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356587"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="11449-103">Exemple de fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="11449-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="11449-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11449-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11449-105">Cet exemple utilise des fichiers et des répertoires pour transmettre et recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="11449-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="11449-106">Il implémente et inscrit un préprocesseur très simple qui ajoute une ligne de texte à chaque message sortant.</span><span class="sxs-lookup"><span data-stu-id="11449-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="11449-107">L’exemple montre comment fractionner le contenu des messages entre le format TNEF (Transport Neutral Encapsulation Format) et le texte.</span><span class="sxs-lookup"><span data-stu-id="11449-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="11449-108">Il prend également en charge toutes les options de configuration (feuilles de propriétés, assistants et configuration par programme) et les options de message.</span><span class="sxs-lookup"><span data-stu-id="11449-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="11449-109">Il ne prend pas en charge les interfaces de transport à distance.</span><span class="sxs-lookup"><span data-stu-id="11449-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="11449-110">Vous pouvez télécharger cet exemple à partir d’exemples de [code MAPI (Outlook Messaging API).](https://go.microsoft.com/fwlink/?LinkId=129740)</span><span class="sxs-lookup"><span data-stu-id="11449-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11449-111">Exécutable :</span><span class="sxs-lookup"><span data-stu-id="11449-111">Executable:</span></span>  <br/> |<span data-ttu-id="11449-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="11449-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="11449-113">Répertoire de code source :</span><span class="sxs-lookup"><span data-stu-id="11449-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="11449-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="11449-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="11449-115">Langue :</span><span class="sxs-lookup"><span data-stu-id="11449-115">Language:</span></span>  <br/> |<span data-ttu-id="11449-116">C++</span><span class="sxs-lookup"><span data-stu-id="11449-116">C++</span></span>  <br/> |
|<span data-ttu-id="11449-117">Plateformes :</span><span class="sxs-lookup"><span data-stu-id="11449-117">Platforms:</span></span>  <br/> |<span data-ttu-id="11449-118">Visual Studio 2008 à compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="11449-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="11449-119">Fonctionnalités prise en charge</span><span class="sxs-lookup"><span data-stu-id="11449-119">Supported Features</span></span>

<span data-ttu-id="11449-120">Cet exemple prend en charge les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="11449-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="11449-121">Fonctionnalités de base telles que l’envoi, la réception et l’interrogation de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="11449-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="11449-122">Configuration interactive et par programme.</span><span class="sxs-lookup"><span data-stu-id="11449-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="11449-123">Interface **IMAPIStatus,** à l’exception du paramètre de propriété.</span><span class="sxs-lookup"><span data-stu-id="11449-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="11449-124">Pour plus d’informations, voir [l’interface IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="11449-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="11449-125">Sécurité des threads.</span><span class="sxs-lookup"><span data-stu-id="11449-125">Thread safety.</span></span>
    
- <span data-ttu-id="11449-126">Journalisation des événements dans un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="11449-126">Event logging to a text file.</span></span> <span data-ttu-id="11449-127">Le fichier est automatiquement limité à une taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="11449-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="11449-128">Toutes les sessions de transport utilisent le même fichier.</span><span class="sxs-lookup"><span data-stu-id="11449-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="11449-129">Fonctionnalités non pris en compte</span><span class="sxs-lookup"><span data-stu-id="11449-129">Unsupported Features</span></span>

<span data-ttu-id="11449-130">Cet exemple ne prend pas en charge la détection asynchrone des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="11449-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="11449-131">**Pour installer l’exemple de fournisseur de transport**</span><span class="sxs-lookup"><span data-stu-id="11449-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="11449-132">Pour télécharger l’exemple de fournisseur de transport, voir [Téléchargement des exemples MAPI Outlook.](downloading-the-outlook-mapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="11449-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="11449-133">Recherchez le dossier dans lequel vous avez enregistré les exemples MAPI Outlook.</span><span class="sxs-lookup"><span data-stu-id="11449-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="11449-134">Cliquez avec le bouton droit sur le dossier zip du numéro de **\< \> version d’OutlookMAPISamples,** puis cliquez sur **Extraire tout.**</span><span class="sxs-lookup"><span data-stu-id="11449-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="11449-135">Cliquez **sur Parcourir,** sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple, puis cliquez sur **Extraire.**</span><span class="sxs-lookup"><span data-stu-id="11449-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="11449-136">Exécutez Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="11449-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="11449-137">Dans Visual Studio 2008, cliquez sur **Fichier,** sélectionnez **Ouvrir,** puis cliquez sur **Projet/Solution.**</span><span class="sxs-lookup"><span data-stu-id="11449-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="11449-138">Accédez à l’emplacement où vous avez enregistré l’exemple, cliquez **sur mrxp32.vcproj,** puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="11449-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="11449-139">Dans **le** menu Créer, cliquez sur **Configuration Manager.**</span><span class="sxs-lookup"><span data-stu-id="11449-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="11449-140">Dans la **boîte de dialogue Configuration Manager,** allez à la ligne **mrxp32,** puis, dans la colonne **Configuration,** sélectionnez **Libérer,** puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="11449-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="11449-141">Dans le menu **Générer**, cliquez sur **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="11449-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="11449-142">Dans la **boîte de dialogue Enregistrer le fichier sous,** cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="11449-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="11449-143">Dans le dossier où vous avez enregistré l’exemple, cliquez avec le bouton droit sur le fichier de lot d’installation et cliquez sur **Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="11449-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="11449-144">Dans la boîte **de dialogue Contrôle de compte** d’utilisateur, cliquez sur **Continuer.**</span><span class="sxs-lookup"><span data-stu-id="11449-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="11449-145">**install.bat** copie le fichier .dll dans le dossier d Microsoft Office d’installation par défaut, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="11449-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="11449-146">Si vous avez installé les produits Office à un autre emplacement, cliquez avec le bouton droit sur **install.bat** puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="11449-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="11449-147">Le fichier s’ouvre dans le Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="11449-147">The file opens in Notepad.</span></span> <span data-ttu-id="11449-148">Remplacez le chemin d’installation par défaut par le chemin d’installation utilisé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="11449-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="11449-149">**Pour configurer le fournisseur de transport dans Outlook**</span><span class="sxs-lookup"><span data-stu-id="11449-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="11449-150">Dans le menu **Outils** d’Outlook, cliquez **sur Paramètres du compte.**</span><span class="sxs-lookup"><span data-stu-id="11449-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="11449-151">Dans la **boîte de dialogue Paramètres du** compte, sous **l’onglet Courrier,** cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="11449-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="11449-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport,** and then click **Next**.</span><span class="sxs-lookup"><span data-stu-id="11449-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="11449-153">Dans la boîte de dialogue Configuration de **transport MRXP,** tapez un **nom complet d’utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="11449-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="11449-154">Sous **Chemin d’accès à la boîte de réception (partage UNC),** entrez un chemin d’accès au dossier.</span><span class="sxs-lookup"><span data-stu-id="11449-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="11449-155">Il peut également s’agit d’un chemin d’accès à un dossier local.</span><span class="sxs-lookup"><span data-stu-id="11449-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="11449-156">Ce chemin d’accès doit exister.</span><span class="sxs-lookup"><span data-stu-id="11449-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="11449-157">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="11449-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="11449-158">Dans la boîte **de dialogue Ajouter un compte** de messagerie, cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="11449-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="11449-159">Cliquez **sur Terminer,** puis sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="11449-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="11449-160">Pour commencer à utiliser le compte MRXP, quittez et redémarrez Outlook.</span><span class="sxs-lookup"><span data-stu-id="11449-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="11449-161">**Pour utiliser l’exemple de fournisseur de transport pour envoyer un message dans Outlook**</span><span class="sxs-lookup"><span data-stu-id="11449-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="11449-162">Dans **le** menu Fichier, cliquez **sur Nouveau,** puis sur **Message électronique.**</span><span class="sxs-lookup"><span data-stu-id="11449-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="11449-163">Dans la **zone À,** tapez le nom du destinataire au format **[MRXP : \< ADRESSE \> ]**.</span><span class="sxs-lookup"><span data-stu-id="11449-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="11449-164">L’adresse est le partage UNC ou le chemin d’accès au dossier local de la boîte de réception du destinataire.</span><span class="sxs-lookup"><span data-stu-id="11449-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="11449-165">Si l’adresse insère des deux-points ou des barre obliques inverses, vous devez insérer une barre oblique inverse avant chaque deux-points ou barre oblique inverse.</span><span class="sxs-lookup"><span data-stu-id="11449-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="11449-166">Par exemple, pour envoyer des messages à [MRXP:C:\Mail\myDir], vous devez taper  `[MRXP:C\:\\Mail\\myDir]` .</span><span class="sxs-lookup"><span data-stu-id="11449-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="11449-167">L’adresse du destinataire doit exister.</span><span class="sxs-lookup"><span data-stu-id="11449-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="11449-168">Cliquez **sur Compte,** puis sur Exemple de **transport MRXP.**</span><span class="sxs-lookup"><span data-stu-id="11449-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="11449-169">Tapez votre message, puis cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="11449-169">Type your message and click **Send**.</span></span> <span data-ttu-id="11449-170">Le message est envoyé à l’aide du fournisseur de transport MRXP.</span><span class="sxs-lookup"><span data-stu-id="11449-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="11449-171">**Pour utiliser l’exemple de fournisseur de transport pour recevoir un message dans Outlook**</span><span class="sxs-lookup"><span data-stu-id="11449-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="11449-172">Dans **le** menu Fichier, cliquez **sur Nouveau,** puis sur **Message électronique.**</span><span class="sxs-lookup"><span data-stu-id="11449-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="11449-173">Tapez votre message.</span><span class="sxs-lookup"><span data-stu-id="11449-173">Type your message.</span></span>
    
3. <span data-ttu-id="11449-174">Cliquez sur **le Microsoft Office,** cliquez sur Enregistrer  **sous,** puis sur Enregistrer sous pour enregistrer le fichier dans le dossier de boîte de réception que vous avez spécifié lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="11449-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="11449-175">Dans la **boîte de dialogue Enregistrer sous,** accédez au partage UNC ou au dossier local que vous définissez comme boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="11449-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="11449-176">In the **Save as type drop** down, click Outlook Message **Format**.</span><span class="sxs-lookup"><span data-stu-id="11449-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="11449-177">Tapez un nom pour le fichier, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="11449-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="11449-178">Le fichier est enregistré dans le dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="11449-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="11449-179">Le fournisseur de transport MRXP envoie le message à votre boîte de réception dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="11449-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    


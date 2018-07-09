---
title: MFCMAPI comme un exemple de code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fc92cc8deb3d12c4bc8fca4c680fd4a675b4a578
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784884"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="7144f-103">MFCMAPI comme un exemple de code</span><span class="sxs-lookup"><span data-stu-id="7144f-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="7144f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7144f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7144f-105">L’exemple MFCMAPI utilise l’API de messagerie pour accéder aux magasins MAPI via une interface utilisateur graphique.</span><span class="sxs-lookup"><span data-stu-id="7144f-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="7144f-106">Après avoir téléchargé cet exemple, vous pouvez utiliser les fichiers sources pour examiner les cas de l’utilisation d’exemple pour la plupart des interfaces MAPI et références.</span><span class="sxs-lookup"><span data-stu-id="7144f-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="7144f-107">Pour plus d’informations, voir [Interfaces MAPI](mapi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7144f-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7144f-108">Plateformes :</span><span class="sxs-lookup"><span data-stu-id="7144f-108">Platforms:</span></span>  <br/> |<span data-ttu-id="7144f-109">Microsoft Visual Studio 2008 pour compiler pour Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="7144f-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="7144f-110">Pour télécharger MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7144f-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="7144f-111">Dans la page [MFCMAPI](http://codeplex.com/MFCMAPI) , cliquez sur l’onglet **Code Source** .</span><span class="sxs-lookup"><span data-stu-id="7144f-111">On the [MFCMAPI](http://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="7144f-112">Sous **Archivages récents**, cliquez sur **Télécharger** pour la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="7144f-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="7144f-113">Lisez le contrat de licence, puis cliquez sur **J’accepte**.</span><span class="sxs-lookup"><span data-stu-id="7144f-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="7144f-114">Dans la boîte de dialogue **Téléchargement de fichier** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7144f-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="7144f-115">Dans la boîte de dialogue **Enregistrer sous** , recherchez le dossier dans lequel vous souhaitez enregistrer les fichiers sources, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7144f-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="7144f-116">Dans la boîte de dialogue **Téléchargement terminé** , cliquez sur **Ouvrir le dossier**.</span><span class="sxs-lookup"><span data-stu-id="7144f-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="7144f-117">Vous pouvez également cliquer sur **Fermer** pour fermer la boîte de dialogue et de localiser les fichiers sources compressés dans le dossier que vous les avez enregistrés dans.</span><span class="sxs-lookup"><span data-stu-id="7144f-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="7144f-118">Avec le bouton droit le **MFCMAPI -\<numéro de version\>.zip** du fichier, puis cliquez sur **Extraire tout**.</span><span class="sxs-lookup"><span data-stu-id="7144f-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="7144f-119">Dans la boîte de dialogue qui s’affiche, cliquez sur **Extraire** pour extraire les fichiers dans le dossier qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7144f-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="7144f-120">Vous pouvez également cliquer sur **Parcourir** pour sélectionner ou créer un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="7144f-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="7144f-121">Exécutez Visual Studio 2008 en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="7144f-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="7144f-122">Si votre ordinateur exécute Windows XP, vous devez être connecté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="7144f-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="7144f-123">Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu’administrateur et vous devez avec le bouton droit de l’icône de Visual Studio 2008, puis cliquez sur **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="7144f-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="7144f-124">Dans Visual Studio 2008, cliquez sur **fichier**, pointez sur **Ouvrir**, puis cliquez sur **Projet/Solution**.</span><span class="sxs-lookup"><span data-stu-id="7144f-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="7144f-125">Accédez à l’emplacement où vous avez enregistré l’exemple, sélectionnez **MFCMapi.vcproj**, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="7144f-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="7144f-126">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="7144f-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="7144f-127">Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7144f-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="7144f-128">Pour utiliser MFCMAPI comme un exemple de code</span><span class="sxs-lookup"><span data-stu-id="7144f-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="7144f-129">Dans **L’Explorateur de solutions**, développez le projet **MFCMapi** et examiner les fichiers dans les nœuds de **Fichiers d’en-tête**, les **Fichiers de ressources**et les **Fichiers sources** pour les scénarios de programmation.</span><span class="sxs-lookup"><span data-stu-id="7144f-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="7144f-130">De nombreuses rubriques de méthode dans la section [Interfaces MAPI](mapi-interfaces.md) pointent sur les fichiers source MFCMAPI pour des exemples de programmation.</span><span class="sxs-lookup"><span data-stu-id="7144f-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="7144f-131">Par exemple, dans [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) , vous êtes invité à examiner la fonction `CMsgStoreDlg::OnDisplayReceiveFolderTable` dans le fichier MsgStoreDlg.cpp.</span><span class="sxs-lookup"><span data-stu-id="7144f-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7144f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7144f-132">See also</span></span>

- [<span data-ttu-id="7144f-133">Exemples MAPI</span><span class="sxs-lookup"><span data-stu-id="7144f-133">MAPI Samples</span></span>](mapi-samples.md)


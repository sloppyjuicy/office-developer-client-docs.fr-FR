---
title: MFCMAPI comme exemple de code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356860"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="3f77e-103">MFCMAPI comme exemple de code</span><span class="sxs-lookup"><span data-stu-id="3f77e-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="3f77e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f77e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f77e-105">L'exemple MFCMAPI utilise l'API de messagerie pour fournir l'accès aux magasins MAPI via une interface utilisateur graphique.</span><span class="sxs-lookup"><span data-stu-id="3f77e-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="3f77e-106">Une fois que vous avez téléchargé cet exemple, vous pouvez utiliser les fichiers sources pour examiner des exemples de cas d'utilisation pour de nombreuses interfaces et références MAPI.</span><span class="sxs-lookup"><span data-stu-id="3f77e-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="3f77e-107">Pour plus d'informations, consultez la rubrique [interfaces MAPI](mapi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="3f77e-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f77e-108">Formes</span><span class="sxs-lookup"><span data-stu-id="3f77e-108">Platforms:</span></span>  <br/> |<span data-ttu-id="3f77e-109">Microsoft Visual Studio 2008 pour la compilation pour Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="3f77e-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="3f77e-110">Pour télécharger MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3f77e-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="3f77e-111">Sur la page [MFCMAPI](https://codeplex.com/MFCMAPI) , cliquez sur l'onglet **code source** .</span><span class="sxs-lookup"><span data-stu-id="3f77e-111">On the [MFCMAPI](https://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="3f77e-112">Sous **archivAges récents**, cliquez sur **Télécharger** pour la build la plus récente.</span><span class="sxs-lookup"><span data-stu-id="3f77e-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="3f77e-113">Lisez le contrat de licence, puis cliquez sur **J'accepte**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="3f77e-114">Dans la boîte de dialogue **Téléchargement de fichiers**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="3f77e-115">Dans la boîte de dialogue **Enregistrer sous** , recherchez le dossier dans lequel vous souhaitez enregistrer les fichiers sources, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="3f77e-116">Dans la boîte de dialogue **Téléchargement terminé** , cliquez sur **ouvrir le dossier**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="3f77e-117">Vous pouvez également cliquer sur **Fermer** pour fermer la boîte de dialogue et rechercher les fichiers sources Zippés dans le dossier dans lequel vous les avez enregistrés.</span><span class="sxs-lookup"><span data-stu-id="3f77e-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="3f77e-118">Cliquez avec le bouton droit sur le fichier **MFCMAPI. zip du\<numéro\>de version** , puis cliquez sur **extraire tout**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="3f77e-119">Dans la boîte de dialogue qui s'affiche, cliquez sur **extraire** pour extraire les fichiers dans le dossier affiché.</span><span class="sxs-lookup"><span data-stu-id="3f77e-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="3f77e-120">Vous pouvez également cliquer sur **Parcourir** pour sélectionner ou créer un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="3f77e-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="3f77e-121">Exécutez Visual Studio 2008 en tant qu'administrateur.</span><span class="sxs-lookup"><span data-stu-id="3f77e-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="3f77e-122">Si votre ordinateur fonctionne sous Windows XP, vous devez être connecté en tant qu'administrateur.</span><span class="sxs-lookup"><span data-stu-id="3f77e-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="3f77e-123">Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu'administrateur et vous devez cliquer avec le bouton droit sur l'icône Visual Studio 2008, puis cliquer sur **exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="3f77e-124">Dans Visual Studio 2008, cliquez sur **fichier**, pointEz sur **ouvrir**, puis cliquez sur **projet/solution**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="3f77e-125">Naviguez jusqu'à l'emplacement où vous avez enregistré l'exemple, sélectionnez **MFCMapi. vcproj**, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="3f77e-126">Dans le menu **Générer**, cliquez sur **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="3f77e-127">Dans la boîte de dialogue **enregistrer le fichier sous** , cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3f77e-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="3f77e-128">Pour utiliser MFCMAPI comme exemple de code</span><span class="sxs-lookup"><span data-stu-id="3f77e-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="3f77e-129">Dans **l'Explorateur de solutions**, développez le projet **MFCMapi** et examinez les fichiers des nœuds **fichiers d'en-tête**, **fichiers de ressources**et **fichiers sources** pour les scénarios de programmation.</span><span class="sxs-lookup"><span data-stu-id="3f77e-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="3f77e-130">De nombreuses rubriques de méthode dans la section [MAPI interfaces](mapi-interfaces.md) pointent vers les fichiers source MFCMAPI pour des exemples de programmation.</span><span class="sxs-lookup"><span data-stu-id="3f77e-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="3f77e-131">Par exemple, dans [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) vous êtes invité à examiner la fonction `CMsgStoreDlg::OnDisplayReceiveFolderTable` dans le fichier MsgStoreDlg. cpp.</span><span class="sxs-lookup"><span data-stu-id="3f77e-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f77e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f77e-132">See also</span></span>

- [<span data-ttu-id="3f77e-133">Exemples MAPI (en anglais)</span><span class="sxs-lookup"><span data-stu-id="3f77e-133">MAPI Samples</span></span>](mapi-samples.md)


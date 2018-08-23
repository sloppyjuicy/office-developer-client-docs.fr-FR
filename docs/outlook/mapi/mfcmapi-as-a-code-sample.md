---
title: MFCMAPI comme un exemple de code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b4d46dc8a84b52605d09a694e6873cb3813ae5b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578114"
---
# <a name="mfcmapi-as-a-code-sample"></a>MFCMAPI comme un exemple de code
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’exemple MFCMAPI utilise l’API de messagerie pour accéder aux magasins MAPI via une interface utilisateur graphique. Après avoir téléchargé cet exemple, vous pouvez utiliser les fichiers sources pour examiner les cas de l’utilisation d’exemple pour la plupart des interfaces MAPI et références. Pour plus d’informations, voir [Interfaces MAPI](mapi-interfaces.md).
  
|||
|:-----|:-----|
|Plateformes :  <br/> |Microsoft Visual Studio 2008 pour compiler pour Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
### <a name="to-download-mfcmapi"></a>Pour télécharger MFCMAPI
  
1. Dans la page [MFCMAPI](http://codeplex.com/MFCMAPI) , cliquez sur l’onglet **Code Source** . 
    
2. Sous **Archivages récents**, cliquez sur **Télécharger** pour la version la plus récente. 
    
3. Lisez le contrat de licence, puis cliquez sur **J’accepte**.
    
4. Dans la boîte de dialogue **Téléchargement de fichier** , cliquez sur **Enregistrer**. Dans la boîte de dialogue **Enregistrer sous** , recherchez le dossier dans lequel vous souhaitez enregistrer les fichiers sources, puis cliquez sur **Enregistrer**.
    
5. Dans la boîte de dialogue **Téléchargement terminé** , cliquez sur **Ouvrir le dossier**. Vous pouvez également cliquer sur **Fermer** pour fermer la boîte de dialogue et de localiser les fichiers sources compressés dans le dossier que vous les avez enregistrés dans. 
    
6. Avec le bouton droit le **MFCMAPI -\<numéro de version\>.zip** du fichier, puis cliquez sur **Extraire tout**. Dans la boîte de dialogue qui s’affiche, cliquez sur **Extraire** pour extraire les fichiers dans le dossier qui s’affiche. Vous pouvez également cliquer sur **Parcourir** pour sélectionner ou créer un autre dossier. 
    
7. Exécutez Visual Studio 2008 en tant qu’administrateur.
    
   > [!NOTE]
   > Si votre ordinateur exécute Windows XP, vous devez être connecté en tant qu’administrateur. Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu’administrateur et vous devez avec le bouton droit de l’icône de Visual Studio 2008, puis cliquez sur **Exécuter en tant qu’administrateur**. 
  
8. Dans Visual Studio 2008, cliquez sur **fichier**, pointez sur **Ouvrir**, puis cliquez sur **Projet/Solution**.
    
9. Accédez à l’emplacement où vous avez enregistré l’exemple, sélectionnez **MFCMapi.vcproj**, puis cliquez sur **Ouvrir**.
    
10. On the **Build** menu, click **Build Solution**.
    
11. Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>Pour utiliser MFCMAPI comme un exemple de code
  
Dans **L’Explorateur de solutions**, développez le projet **MFCMapi** et examiner les fichiers dans les nœuds de **Fichiers d’en-tête**, les **Fichiers de ressources**et les **Fichiers sources** pour les scénarios de programmation. 
  
De nombreuses rubriques de méthode dans la section [Interfaces MAPI](mapi-interfaces.md) pointent sur les fichiers source MFCMAPI pour des exemples de programmation. Par exemple, dans [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) , vous êtes invité à examiner la fonction `CMsgStoreDlg::OnDisplayReceiveFolderTable` dans le fichier MsgStoreDlg.cpp. 
  
## <a name="see-also"></a>Voir aussi

- [Exemples MAPI (en anglais)](mapi-samples.md)


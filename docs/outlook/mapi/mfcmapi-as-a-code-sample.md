---
title: MFCMAPI comme exemple de code
description: L’exemple MFCMAPI utilise l’API de messagerie pour fournir l’accès aux magasins MAPI via une interface utilisateur graphique.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
ms.openlocfilehash: dd96a4e8dfec634872b3d97fa9192c0559c771d0
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828503"
---
# <a name="mfcmapi-as-a-code-sample"></a>MFCMAPI comme exemple de code
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’exemple MFCMAPI utilise l’API de messagerie pour fournir l’accès aux magasins MAPI via une interface utilisateur graphique. Après avoir téléchargé cet exemple, vous pouvez utiliser les fichiers sources pour examiner des exemples de cas d’utilisation pour de nombreuses interfaces et références MAPI. Pour plus d’informations, consultez [Interfaces MAPI](mapi-interfaces.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Plateformes :  <br/> |Microsoft Visual Studio 2008 à compiler pour Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
### <a name="to-download-mfcmapi"></a>Pour télécharger MFCMAPI
  
1. Dans la page [MFCMAPI](https://codeplex.com/MFCMAPI) , cliquez sur l’onglet **Code source** . 
    
2. Sous **Archivages récents**, cliquez sur **Télécharger** pour la build la plus récente. 
    
3. Lisez le contrat de licence, puis cliquez sur **J’accepte**.
    
4. Dans la boîte de dialogue **Téléchargement de fichiers**, cliquez sur **Enregistrer**. Dans la boîte **de dialogue Enregistrer sous** , recherchez le dossier dans lequel vous souhaitez enregistrer les fichiers sources, puis cliquez sur **Enregistrer**.
    
5. Dans la boîte de dialogue **Télécharger l’intégralité** , cliquez sur **Ouvrir le dossier**. Vous pouvez également cliquer sur **Fermer** pour fermer la boîte de dialogue et localiser les fichiers sources compressés dans le dossier dans lequel vous les avez enregistrés. 
    
6. Cliquez avec le bouton droit sur le fichier **MFCMAPI-\<version number\>.zip** , puis cliquez sur **Extraire tout**. Dans la boîte de dialogue qui s’affiche, cliquez sur **Extraire** pour extraire les fichiers dans le dossier qui s’affiche. Vous pouvez également cliquer sur **Parcourir** pour sélectionner ou créer un autre dossier. 
    
7. Exécutez Visual Studio 2008 en tant qu’administrateur.
    
   > [!NOTE]
   > Si votre ordinateur s’exécute Windows XP, vous devez être connecté en tant qu’administrateur. Si votre ordinateur s’exécute Windows Vista, vous devez être connecté en tant qu’administrateur et cliquer avec le bouton droit sur l’icône Visual Studio 2008, puis cliquer sur **Exécuter en tant qu’administrateur**. 
  
8. Dans Visual Studio 2008, cliquez sur **Fichier**, pointez sur **Ouvrir**, puis cliquez sur **Project/Solution**.
    
9. Accédez à l’emplacement où vous avez enregistré l’exemple, sélectionnez **MFCMapi.vcproj**, puis cliquez sur **Ouvrir**.
    
10. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
11. Dans la boîte **de dialogue Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>Pour utiliser MFCMAPI comme exemple de code
  
Dans **Explorateur de solutions**, développez le projet **MFCMapi** et examinez les fichiers des **nœuds Fichiers** d’en-tête, **Fichiers de ressources** et **Fichiers sources** pour les scénarios de programmation. 
  
De nombreuses rubriques de méthode de la section [Interfaces MAPI](mapi-interfaces.md) pointent vers des fichiers sources MFCMAPI pour des exemples de programmation. Par exemple, dans [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) , vous êtes invité à examiner la fonction  `CMsgStoreDlg::OnDisplayReceiveFolderTable` dans le fichier MsgStoreDlg.cpp. 
  
## <a name="see-also"></a>Voir aussi

- [Exemples MAPI](mapi-samples.md)


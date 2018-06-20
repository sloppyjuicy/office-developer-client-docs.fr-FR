---
title: Exemple de fournisseur de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b3c907b0a53a41a52516b23ffb1cf7400d887d89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784883"
---
# <a name="message-store-provider-sample"></a>Exemple de fournisseur de banque de messages

  
  
**S’applique à**: Outlook 
  
Le fournisseur de banque PST encapsulé exemple utilise un fournisseur de fichier (.pst) de dossiers personnels en tant que serveur principal pour le stockage des données. Le fournisseur de banque PST encapsulé doit être utilisé avec l’API de réplication. 
  
L’API de réplication permet de répliquer des éléments d’un référentiel de données principale dans le magasin de fichiers PST de Microsoft Outlook. Vous utilisez l’API de réplication pour répliquer les données dans une banque de dossiers personnels dédiée et garder une trace de l’état de synchronisation. Pour plus d’informations, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).
  
La plupart des fonctions dans le fournisseur de banque PST encapsulé exemple transmettre leurs arguments directement au fournisseur sous-jacent PST. Certaines fonctions requièrent une implémentation spéciale et sont décrites dans les rubriques suivantes.
  
|||
|:-----|:-----|
|Fichier exécutable :  <br/> |WrpPST32.dll  <br/> |
|Répertoire de code source :  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Langue :  <br/> |C++  <br/> |
|Plateformes :  <br/> |Microsoft Visual Studio 2008 pour compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Fonctionnalités prises en charge

Cet exemple prend en charge de Microsoft Outlook 2010 64 bits et maintenant a été modifié pour Outlook 2013. Consultez les rubriques suivantes pour plus d’informations :
  
- [À propos de l’API de réplication](about-the-replication-api.md)
    
- [L’initialisation d’un fournisseur de banque de dossiers personnels encapsulé](initializing-a-wrapped-pst-store-provider.md)
    
- [Se connecter à un fournisseur de banque de dossiers personnels encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [À l’aide d’un fournisseur de banque de dossiers personnels encapsulé](using-a-wrapped-pst-store-provider.md)
    
- [Arrêt d’un fournisseur de banque de dossiers personnels encapsulé](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Pour installer le fournisseur de banque exemple encapsulé PST**
  
1. Pour télécharger l’exemple entourées de fournisseur PST, voir [télécharger les exemples de MAPI Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Recherchez le dossier où vous avez enregistré les exemples de MAPI Outlook. Avec le bouton droit la **OutlookMAPISamples -\<numéro de version\> ** zip du dossier, puis cliquez sur **Extraire tout**.
    
3. Cliquez sur **Parcourir**, sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple, puis cliquez sur **Extraire**.
    
4. Exécutez Microsoft Visual Studio 2008.
    
5. Dans Microsoft Visual Studio 2008, cliquez sur **fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.
    
6. Accédez à l’emplacement où vous avez enregistré l’exemple et cliquez sur **WrapPST.vcproj**, puis cliquez sur **Ouvrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
9. Dans le dossier où vous avez enregistré l’exemple, cliquez sur le fichier **install.bat** , puis sur **Exécuter en tant qu’administrateur**.
    
10. Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.
    


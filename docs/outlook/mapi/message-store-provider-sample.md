---
title: Exemple de fournisseur de magasin de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c9cd4c62dfff127763494c2edab0a3ec47ee9413
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571415"
---
# <a name="message-store-provider-sample"></a>Exemple de fournisseur de magasin de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’exemple de fournisseur de magasins PST wrapped utilise un fournisseur de fichiers de dossiers personnels (PST) comme système de stockage des données. Le fournisseur de magasin PST wrapped doit être utilisé avec l’API de réplication. 
  
L’API de réplication vous permet de répliquer des éléments à partir d’un référentiel de données back end dans un magasin PST Outlook Microsoft. Vous utilisez l’API de réplication pour répliquer les données dans un magasin PST dédié et suivre l’état de synchronisation. Pour plus d’informations, voir [à propos de l’API de réplication.](about-the-replication-api.md)
  
La plupart des fonctions dans l’exemple de fournisseur de magasin PST Wrapped passent leurs arguments directement au fournisseur PST sous-jacent. Certaines fonctions nécessitent une implémentation spéciale et sont décrites dans les rubriques suivantes.
  
|||
|:-----|:-----|
|Exécutable :  <br/> |WrpPST32.dll  <br/> |
|Répertoire de code source :  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Langue :  <br/> |C++  <br/> |
|Plateformes :  <br/> |Microsoft Visual Studio 2008 à compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Fonctionnalités prise en charge

Cet exemple prend en charge Microsoft Outlook 2010 64 bits et a été révisé Outlook 2013. Pour plus d’informations, consultez les rubriques suivantes :
  
- [À propos de l’API de réplication](about-the-replication-api.md)
    
- [Initialisation d’un fournisseur de magasin PST wrapped](initializing-a-wrapped-pst-store-provider.md)
    
- [Connexion à un fournisseur de magasin PST wrapped](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Utilisation d’un fournisseur de magasin PST wrapped](using-a-wrapped-pst-store-provider.md)
    
- [Arrêt d’un fournisseur de magasin PST wrapped](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Pour installer l’exemple de fournisseur de magasin PST Wrapped**
  
1. Pour télécharger l’exemple de fournisseur PST Wrapped, voir Téléchargement des exemples [Outlook MAPI.](downloading-the-outlook-mapi-samples.md)
    
2. Recherchez le dossier dans lequel vous avez enregistré Outlook exemples MAPI. Cliquez avec le bouton droit **sur \<version number\> le dossier Zip OutlookMAPISamples,** puis cliquez sur **Extraire tout.**
    
3. Cliquez **sur Parcourir,** sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple, puis cliquez sur **Extraire.**
    
4. Exécutez Microsoft Visual Studio 2008.
    
5. Dans Microsoft Visual Studio 2008, cliquez sur **Fichier,** sélectionnez **Ouvrir,** puis cliquez sur **Project/Solution.**
    
6. Accédez à l’emplacement où vous avez enregistré l’exemple, cliquez sur **WrapPST.vcproj,** puis cliquez sur **Ouvrir**.
    
7. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
8. Dans la **boîte de dialogue Enregistrer le fichier sous,** cliquez sur **Enregistrer.**
    
9. Dans le dossier où vous avez enregistré l’exemple, cliquez avec le bouton droit sur **install.bat** fichier, puis cliquez sur **Exécuter en tant qu’administrateur.**
    
10. Dans la boîte **de dialogue Contrôle de compte** d’utilisateur, cliquez sur **Continuer.**
    


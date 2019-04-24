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
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356937"
---
# <a name="message-store-provider-sample"></a>Exemple de fournisseur de banque de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'exemple de fournisseur de banque d'informations PST encapsulé utilise un fournisseur de fichiers de dossiers personnels (PST) comme serveur principal pour le stockage des données. Le fournisseur de magasins PST encapsulé doit être utilisé avec l'API de réPlication. 
  
L'API de réPlication vous permet de répliquer des éléments à partir d'un référentiel de données principal dans un magasin Microsoft Outlook PST. L'API de réPlication permet de répliquer les données dans un magasin PST dédié et de suivre l'état de synchronisation. Pour plus d'informations, consultez [la rubrique à propos de l'API](about-the-replication-api.md)de réplication.
  
La plupart des fonctions dans l'exemple de fournisseur de magasins PST encapsulé passent leurs arguments directement au fournisseur PST sous-jacent. Certaines fonctions nécessitent une implémentation spéciale et sont décrites dans les rubriques suivantes.
  
|||
|:-----|:-----|
|Exécutable  <br/> |WrpPST32. dll  <br/> |
|Répertoire de code source:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Langue  <br/> |C++  <br/> |
|Formes  <br/> |Microsoft Visual Studio 2008 pour la compilation pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Fonctionnalités prises en charge

Cet exemple prend en charge Microsoft Outlook 2010 64 bits et est maintenant révisé pour Outlook 2013. Pour plus d'informations, consultez les rubriques suivantes:
  
- [À propos de l’API de réplication](about-the-replication-api.md)
    
- [Initialisation d'un fournisseur de magasins PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
    
- [Connexion à un fournisseur de magasins PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Utilisation d'un fournisseur de magasins PST encapsulé](using-a-wrapped-pst-store-provider.md)
    
- [Arrêt d'un fournisseur de magasins PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Pour installer l'exemple de fournisseur de magasins PST encapsulé**
  
1. Pour télécharger l'exemple de fournisseur de fichiers PST encapsulés, consultez [la rubrique téléchargement des exemples MAPI Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Recherchez le dossier dans lequel vous avez enregistré les exemples MAPI Outlook. Cliquez avec le bouton droit sur le dossier zip de **\<\> numéro de version OutlookMAPISamples** , puis cliquez sur **extraire tout**.
    
3. Cliquez sur **Parcourir**, sélectionnez l'emplacement où vous souhaitez enregistrer l'exemple, puis cliquez sur **extraire**.
    
4. Exécutez Microsoft Visual Studio 2008.
    
5. Dans Microsoft Visual Studio 2008, cliquez sur **fichier**, sur **ouvrir**, puis sur **projet/solution**.
    
6. Naviguez jusqu'à l'emplacement où vous avez enregistré l'exemple, cliquez sur **WrapPST. vcproj**, puis cliquez sur **ouvrir**.
    
7. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
8. Dans la boîte de dialogue **enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
9. Dans le dossier où vous avez enregistré l'exemple, cliquez avec le bouton droit sur le fichier **install. bat** , puis cliquez sur **exécuter en tant qu'administrateur**.
    
10. Dans la boîte de dialogue **contrôle de compte d'utilisateur** , cliquez sur **Continuer**.
    


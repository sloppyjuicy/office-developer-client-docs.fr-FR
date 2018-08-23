---
title: Exemple de fournisseur de carnets d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ebbed00fb920994f40b7ae139c7eddd658984b95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566858"
---
# <a name="address-book-provider-sample"></a>Exemple de fournisseur de carnets d’adresses

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cet exemple prend en charge un seul conteneur en lecture seule pour les noms complets et les adresses de messagerie, qui sont lues à partir d’un fichier binaire plat. L’exemple prend en charge les modèles uniques et toutes les options de configuration à l’exception de l’Assistant profil.
  
Vous pouvez télécharger cet exemple à partir des [Exemples de Code Outlook MAPI (Messaging API)](http://go.microsoft.com/fwlink/?LinkId=129740
).
  
|||
|:-----|:-----|
|Fichier exécutable :  <br/> |SABP32.dll  <br/> |
| Répertoire de code source :  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Langue :  <br/> |C++  <br/> |
|Plateformes :  <br/> |Microsoft Visual Studio 2008 pour compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Fonctionnalités prises en charge

Cet exemple prend en charge les fonctionnalités suivantes :
  
- Restrictions de table. L’exemple implémente résolution-correspondance de préfixe et de nom ambigu. Il n’implémente pas la langue de restriction MAPI complète et restrictions sont pris en charge uniquement sur le nom complet.
    
- Une table d’affichage Détails pour les utilisateurs de messagerie. 
    
- Adresses uniques.
    
- Une boîte de dialogue Recherche avancée.
    
- Un [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface. Cette interface est partiellement pris en charge ; ses méthodes **IMAPIProp** sont délégués à l’interface **IPropData** . Pour plus d’informations, voir la [IPropData : IMAPIProp](ipropdataimapiprop.md) interface. 
    
- Configuration interactive et par programmation.
    
## <a name="unsupported-features"></a>Fonctionnalités non prises en charge

Cet exemple ne prend pas en charge les fonctionnalités suivantes :
  
- Tri.
    
- Listes de distribution.
    
- Création, suppression et modification des entrées.
    
- Propriétés à valeurs multiples.
    
- Propriétés nommées.
    
- Faire la distinction entre le prénom et le nom dans les noms complets.
    
 **Pour installer l’exemple de fournisseur de carnet d’adresses**
  
1. Pour télécharger l’exemple de fournisseur de carnet d’adresses, voir [le téléchargement d’exemples MAPI Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Recherchez le dossier où vous avez enregistré les exemples de MAPI Outlook. Avec le bouton droit la **OutlookMAPISamples -\<numéro de version\> ** zip du dossier, puis cliquez sur **Extraire tout**.
    
3. Cliquez sur **Parcourir**, sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple et cliquez sur **Extraire**.
    
4. Exécutez Visual Studio 2008.
    
5. Dans Visual Studio 2008, cliquez sur **fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.
    
6. Accédez à l’emplacement où vous avez enregistré l’exemple et cliquez sur **SABP.vcproj**, puis cliquez sur **Ouvrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
9. Dans le dossier où vous avez enregistré l’exemple, cliquez sur le fichier **install.bat** et cliquez sur **Exécuter en tant qu’administrateur**.
    
10. Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.
    
    > [!NOTE]
    > **Install.bat** cette méthode copie la DLL dans le dossier d’installation par défaut de Microsoft Office, C:\Program Files\Microsoft Office\Office12\. Si vous avez installé des produits Office dans un autre emplacement, cliquez sur **Install.bat** , cliquez sur **Modifier**. Le fichier s’ouvre dans le bloc-notes. Remplacez le chemin d’installation par défaut par le chemin d’installation sur votre ordinateur. 
  


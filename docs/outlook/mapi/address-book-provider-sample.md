---
title: Exemple de fournisseur de carnet d’adresses
description: Exemple de fournisseur de carnet d’adresses qui prend en charge un seul conteneur en lecture seule pour les noms d’affichage et les adresses e-mail, qui sont lus à partir d’un fichier binaire plat.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
ms.openlocfilehash: 1491f89099620363e18ea162d2395c0f7584f3a8
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770466"
---
# <a name="address-book-provider-sample"></a>Exemple de fournisseur de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cet exemple prend en charge un seul conteneur en lecture seule pour les noms d’affichage et les adresses e-mail, qui sont lus à partir d’un fichier binaire plat. L’exemple prend en charge les modèles uniques et toutes les options de configuration à l’exception de l’Assistant Profil.
  
Vous pouvez télécharger cet exemple à partir de [Outlook exemples de code d’API de messagerie (MAPI](https://go.microsoft.com/fwlink/?LinkId=129740
)).
  
|Propriété |Valeur |
|:-----|:-----|
|Exécutable:  <br/> |SABP32.dll  <br/> |
| Répertoire de code source :  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Langue:  <br/> |C++  <br/> |
|Plateformes :  <br/> |Microsoft Visual Studio 2008 à compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Fonctionnalités prises en charge

Cet exemple prend en charge les fonctionnalités suivantes :
  
- Restrictions de table. L’exemple implémente la résolution de correspondance de préfixe et de nom ambigu. Il n’implémente pas le langage de restriction MAPI complet et les restrictions sont prises en charge uniquement sur le nom d’affichage.
    
- Tableau d’affichage des détails pour les utilisateurs de messagerie. 
    
- Adresses uniques.
    
- Boîte de dialogue Recherche avancée.
    
- Interface [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) . Cette interface est partiellement prise en charge ; ses méthodes **IMAPIProp** sont déléguées à l’interface **IPropData** . Pour plus d’informations, consultez l’interface [IPropData : IMAPIProp](ipropdataimapiprop.md) . 
    
- Configuration interactive et programmatique.
    
## <a name="unsupported-features"></a>Fonctionnalités non prises en charge

Cet exemple ne prend pas en charge les fonctionnalités suivantes :
  
- Tri.
    
- Listes de distribution.
    
- Création, suppression et modification d’entrées.
    
- Propriétés avec plusieurs valeurs.
    
- Propriétés nommées.
    
- Distinction entre les prénoms et les noms dans les noms d’affichage.
    
 **Pour installer l’exemple de fournisseur de carnet d’adresses**
  
1. Pour télécharger l’exemple de fournisseur de carnet d’adresses, consultez [Téléchargement des exemples MAPI Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Recherchez le dossier dans lequel vous avez enregistré les Outlook exemples MAPI. Cliquez avec le bouton droit sur le dossier **OutlookMAPISamples-\<version number\>** zip, puis cliquez sur **Extraire tout**.
    
3. Cliquez sur **Parcourir**, sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple, puis cliquez sur **Extraire**.
    
4. Exécutez Visual Studio 2008.
    
5. Dans Visual Studio 2008, cliquez sur **Fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Project/Solution**.
    
6. Accédez à l’emplacement où vous avez enregistré l’exemple, cliquez sur **SABP.vcproj**, puis sur **Ouvrir**.
    
7. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
8. Dans la boîte **de dialogue Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
9. Dans le dossier dans lequel vous avez enregistré l’exemple, cliquez avec le bouton droit sur le fichier **install.bat** , puis cliquez sur **Exécuter en tant qu’administrateur**.
    
10. Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.
    
    > [!NOTE]
    > **Install.bat** copie l'.dll dans le dossier d’installation de Microsoft Office par défaut, C:\Program Files\Microsoft Office\Office12\. Si vous avez installé Office produits à un autre emplacement, cliquez avec le bouton droit sur **Install.bat**, puis cliquez sur **Modifier**. Le fichier s’ouvre dans Bloc-notes. Remplacez le chemin d’installation par défaut par le chemin d’installation utilisé sur votre ordinateur. 
  


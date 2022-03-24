---
title: Exemple de fournisseur de carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6639fa9d316762a1cd6b0abd8dfd7e87722c9312
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63720651"
---
# <a name="address-book-provider-sample"></a>Exemple de fournisseur de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cet exemple prend en charge un conteneur en lecture seule unique pour les noms complets et les adresses e-mail, qui sont lus à partir d’un fichier binaire plat. L’exemple prend en charge les modèles unique et toutes les options de configuration à l’exception de l’Assistant Profil.
  
Vous pouvez télécharger cet exemple à partir [Outlook exemples de code MAPI (Messaging API](https://go.microsoft.com/fwlink/?LinkId=129740
)).
  
|Propriété |Valeur |
|:-----|:-----|
|Exécutable :  <br/> |SABP32.dll  <br/> |
| Répertoire de code source :  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Langue :  <br/> |C++  <br/> |
|Plateformes :  <br/> |Microsoft Visual Studio 2008 à compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Fonctionnalités prise en charge

Cet exemple prend en charge les fonctionnalités suivantes :
  
- Restrictions de tableau. L’exemple implémente la correspondance de préfixe et la résolution de nom ambigu. Il n’implémente pas le langage de restriction MAPI complet et les restrictions sont uniquement prise en charge sur le nom complet.
    
- Tableau d’affichage des détails pour les utilisateurs de messagerie. 
    
- Adresses one-off.
    
- Boîte de dialogue de recherche avancée.
    
- Interface [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) . Cette interface est partiellement prise en charge ; ses **méthodes IMAPIProp** sont déléguées à l’interface **IPropData** . Pour plus d’informations, voir [l’interface IPropData : IMAPIProp](ipropdataimapiprop.md) . 
    
- Configuration interactive et par programme.
    
## <a name="unsupported-features"></a>Fonctionnalités non pris en compte

Cet exemple ne prend pas en charge les fonctionnalités suivantes :
  
- Tri.
    
- Listes de distribution.
    
- Création, suppression et modification d’entrées.
    
- Propriétés avec plusieurs valeurs.
    
- Propriétés nommées.
    
- Faire la distinction entre le prénom et le nom dans les noms d’affichage.
    
 **Pour installer l’exemple de fournisseur de carnet d’adresses**
  
1. Pour télécharger l’exemple de fournisseur de carnet d’adresses, consultez la [Outlook exemples MAPI](downloading-the-outlook-mapi-samples.md).
    
2. Recherchez le dossier dans lequel vous avez enregistré Outlook exemples MAPI. Cliquez avec le bouton droit **sur le dossier Zip OutlookMAPISamples\<version number\>** , puis cliquez **sur Extraire tout**.
    
3. Cliquez **sur Parcourir**, sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple, puis cliquez sur **Extraire**.
    
4. Exécutez Visual Studio 2008.
    
5. Dans Visual Studio 2008, cliquez sur **Fichier,** sélectionnez **Ouvrir**, puis cliquez sur **Project/Solution**.
    
6. Accédez à l’emplacement où vous avez enregistré l’exemple, cliquez sur **SABP.vcproj**, puis cliquez sur **Ouvrir**.
    
7. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
8. Dans la **boîte de dialogue Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
9. Dans le dossier où vous avez enregistré l’exemple, cliquez avec le bouton droit sur **install.bat** fichier, puis cliquez sur **Exécuter en tant qu’administrateur**.
    
10. Dans la boîte **de dialogue Contrôle de compte** d’utilisateur, cliquez sur **Continuer**.
    
    > [!NOTE]
    > **Install.bat** copie la .dll dans le dossier d’installation Microsoft Office défaut, C:\Program Files\Microsoft Office\Office12\. Si vous avez installé Office produits à un autre emplacement, cliquez avec le bouton droit sur **Install.bat** puis cliquez sur **Modifier**. Le fichier s’ouvre en Bloc-notes. Remplacez le chemin d’installation par défaut par le chemin d’installation utilisé sur votre ordinateur. 
  


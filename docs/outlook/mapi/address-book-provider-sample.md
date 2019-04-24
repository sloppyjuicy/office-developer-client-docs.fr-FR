---
title: Exemple de fournisseur de carnet d'adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331107"
---
# <a name="address-book-provider-sample"></a>Exemple de fournisseur de carnet d'adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cet exemple prend en charge un seul conteneur en lecture seule pour les noms d'affichage et les adresses de messagerie, qui sont lus à partir d'un fichier binaire plat. L'exemple prend en charge les modèles uniques et toutes les options de configuration à l'exception de l'Assistant Profil.
  
Vous pouvez télécharger cet exemple à partir d' [exemples de code MAPI (Outlook messagING API)](https://go.microsoft.com/fwlink/?LinkId=129740
).
  
|||
|:-----|:-----|
|Exécutable  <br/> |SABP32. dll  <br/> |
| Répertoire de code source:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Langue  <br/> |C++  <br/> |
|Formes  <br/> |Microsoft Visual Studio 2008 pour la compilation pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Fonctionnalités prises en charge

Cet exemple prend en charge les fonctionnalités suivantes:
  
- Restrictions de table. L'exemple implémente la résolution de préfixe et de nom ambigu. Il n'implémente pas le langage de restriction MAPI complet, et les restrictions ne sont prises en charge que sur le nom d'affichage.
    
- Tableau d'affichage détaillé pour les utilisateurs de messagerie. 
    
- Adresses ponctuelles.
    
- Boîte de dialogue Recherche avancée.
    
- Une interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . Cette interface est partiellement prise en charge; ses méthodes **IMAPIProp** sont déléguées à l'interface **IPropData** . Pour plus d'informations, reportez-vous à l'interface [IPropData: IMAPIProp](ipropdataimapiprop.md) . 
    
- Configuration interactive et par programmation.
    
## <a name="unsupported-features"></a>Fonctionnalités non prises en charge

Cet exemple ne prend pas en charge les fonctionnalités suivantes:
  
- Triant.
    
- Listes de distribution.
    
- La création, la suppression et la modification des entrées;
    
- Propriétés avec plusieurs valeurs.
    
- Propriétés nommées.
    
- Distinction entre le prénom et le nom dans les noms d'affichage.
    
 **Pour installer l'exemple de fournisseur de carnet d'adresses**
  
1. Pour télécharger l'exemple de fournisseur de carnet d'adresses, consultez [la rubrique téléchargement des exemples MAPI Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Recherchez le dossier dans lequel vous avez enregistré les exemples MAPI Outlook. Cliquez avec le bouton droit sur le dossier zip de **\<\> numéro de version OutlookMAPISamples** et cliquez sur **extraire tout**.
    
3. Cliquez sur **Parcourir**, sélectionnez l'emplacement où vous souhaitez enregistrer l'exemple, puis cliquez sur **extraire**.
    
4. Exécutez Visual Studio 2008.
    
5. Dans Visual Studio 2008, cliquez sur **fichier**, sur **ouvrir**, puis sur **projet/solution**.
    
6. Naviguez jusqu'à l'emplacement où vous avez enregistré l'exemple, cliquez sur **SABP. vcproj**, puis cliquez sur **ouvrir**.
    
7. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
8. Dans la boîte de dialogue **enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
9. Dans le dossier où vous avez enregistré l'exemple, cliquez avec le bouton droit sur le fichier **install. bat** , puis cliquez sur **exécuter en tant qu'administrateur**.
    
10. Dans la boîte de dialogue **contrôle de compte d'utilisateur** , cliquez sur **Continuer**.
    
    > [!NOTE]
    > **Install. bat** copie le fichier. dll dans le dossier d'installation par défaut de Microsoft Office, C:\Program Files\Microsoft Office\Office12\. Si vous avez installé les produits Office à un autre emplacement, cliquez avec le bouton droit sur **install. bat** et cliquez sur **modifier**. Le fichier s'ouvre dans le bloc-notes. Remplacez le chemin d'installation par défaut par le chemin d'installation utilisé sur votre ordinateur. 
  


---
title: Exemple de fournisseur de transport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401404"
---
# <a name="transport-provider-sample"></a>Exemple de fournisseur de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cet exemple utilise les fichiers et répertoires pour transmettre et recevoir des messages. Il implémente et enregistre un préprocesseur très simple qui ajoute une ligne de texte à chaque message sortant. L’exemple montre comment fractionner le contenu des messages entre Neutral Encapsulation Format TNEF (Transport) et le texte. Il prend également en charge toutes les options de message et les options de configuration (feuilles de propriétés, les Assistants et la configuration de programmation). Il ne gère pas les interfaces de transport à distance. 
  
Vous pouvez télécharger cet exemple à partir des [Exemples de Code Outlook MAPI (Messaging API)](https://go.microsoft.com/fwlink/?LinkId=129740).
  
|||
|:-----|:-----|
|Fichier exécutable :  <br/> |mrxp32.dll  <br/> |
|Répertoire de code source :  <br/> |SampleTransportProvider\MRXP  <br/> |
|Langue :  <br/> |C++  <br/> |
|Plateformes :  <br/> |Visual Studio 2008 pour compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Fonctionnalités prises en charge

Cet exemple prend en charge les fonctionnalités suivantes :
  
- Les principales fonctionnalités telles que l’envoi et réception d’interrogation pour les nouveaux messages.
    
- Configuration interactive et par programmation.
    
- L’interface **IMAPIStatus** , à l’exception du paramètre de la propriété. Pour plus d’informations, voir la [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface. 
    
- Sécurité des threads.
    
- Journalisation des événements dans un fichier texte. Le fichier est automatiquement limité à une taille spécifiée. Toutes les sessions de transport utilisent le même fichier.
    
## <a name="unsupported-features"></a>Fonctionnalités non prises en charge

Cet exemple ne gère pas la détection asynchrone des messages entrants.
  
 **Pour installer l’exemple de fournisseur de Transport**
  
1. Pour télécharger l’exemple de fournisseur de Transport, consultez [le téléchargement d’exemples MAPI Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Recherchez le dossier où vous avez enregistré les exemples MAPI Outlook. Avec le bouton droit la **OutlookMAPISamples -\<numéro de version\> ** zip du dossier, puis cliquez sur **Extraire tout**.
    
3. Cliquez sur **Parcourir**, sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple et cliquez sur **Extraire**.
    
4. Exécutez Visual Studio 2008.
    
5. Dans Visual Studio 2008, cliquez sur **fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.
    
6. Accédez à l’emplacement où vous avez enregistré l’exemple et cliquez sur **mrxp32.vcproj**, puis cliquez sur **Ouvrir**.
    
7. Dans le menu **Générer** , cliquez sur **Gestionnaire de Configuration**.
    
8. Dans la boîte de dialogue **Gestionnaire de Configuration** , accédez à la ligne **mrxp32** et sélectionner la **version**dans la colonne **Configuration** , puis cliquez sur **Fermer**.
    
9. On the **Build** menu, click **Build Solution**.
    
10. Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
11. Dans le dossier où vous avez enregistré l’exemple, cliquez sur le fichier de commandes d’installation, cliquez sur **Exécuter en tant qu’administrateur**.
    
12. Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.
    
    > [!NOTE]
    > **Install.bat** cette méthode copie la DLL dans le dossier d’installation par défaut de Microsoft Office, C:\Program Files\Microsoft Office\Office12\. Si vous avez installé des produits Office dans un autre emplacement, cliquez sur **install.bat** , cliquez sur **Modifier**. Le fichier s’ouvre dans le bloc-notes. Remplacez le chemin d’installation par défaut par le chemin d’installation sur votre ordinateur. 
  
 **Pour configurer le fournisseur de Transport dans Outlook**
  
1. Dans le menu **Outils** d’Outlook, cliquez sur **Paramètres du compte**.
    
2. Dans la boîte de dialogue **Paramètres du compte** , sous l’onglet **messagerie** , cliquez sur **Nouveau**.
    
3. Sous **Choisir un Service de messagerie** cliquez sur **autres**, sélectionnez **MRXP exemple Transport**, puis cliquez sur **suivant**.
    
4. Dans la boîte de dialogue **Configuration du Transport MRXP** , tapez un **Nom d’utilisateur complet**.
    
5. Sous le **chemin d’accès à la boîte de réception (partage UNC)** , entrez un chemin d’accès du dossier. Cela peut également être un chemin d’accès à un dossier local. 
    
    > [!IMPORTANT]
    > Ce chemin d’accès doit exister. 
  
6. Cliquez sur **OK**.
    
7. Dans la boîte de dialogue **Ajouter un compte de messagerie** , cliquez sur **OK**. Cliquez sur **Terminer** , puis cliquez sur **Fermer**.
    
8. Pour commencer à utiliser le compte MRXP, quittez et redémarrez Outlook.
    
 **Pour utiliser l’exemple de fournisseur de Transport pour envoyer un message dans Outlook**
  
1. Dans le menu **fichier** , cliquez sur **Nouveau**, puis cliquez sur **Message électronique**.
    
2. Dans **la zone** tapez le nom du destinataire en utilisant le format **[MRXP :\<adresse\>]**. L’adresse est le partage UNC ou un chemin d’accès du dossier local à la boîte de réception du destinataire.
    
    > [!NOTE]
    > S’il y a des signes deux-points ou des barres obliques inverses dans l’adresse, vous devez insérer une barre oblique inverse avant chaque point-virgule ou une barre oblique inverse. Par exemple, envoyer un courrier électronique [MRXP:C:\Mail\myDir] vous devez taper `[MRXP:C\:\\Mail\\myDir]`. 
  
    > [!IMPORTANT]
    > L’adresse du destinataire doit exister. 
  
3. Cliquez sur **le compte** , puis sur **MRXP exemple Transport**.
    
4. Tapez votre message, cliquez sur **Envoyer**. Le message est envoyé à l’aide du fournisseur de transport MRXP.
    
 **Pour utiliser l’exemple de fournisseur de Transport pour recevoir un message dans Outlook**
  
1. Dans le menu **fichier** , cliquez sur **Nouveau**, puis cliquez sur **Message électronique**.
    
2. Tapez votre message.
    
3. Cliquez sur le **Bouton Microsoft Office**, cliquez sur **Enregistrer sous**, puis cliquez sur **Enregistrer sous** pour enregistrer le fichier dans le dossier boîte de réception que vous avez spécifié lors de l’installation. 
    
4. Dans la boîte de dialogue **Enregistrer sous** , accédez au partage UNC ou au dossier local que vous avez définie en tant que votre boîte de réception. 
    
5. Dans la liste déroulante **Enregistrer en tant que type** , cliquez sur le **Format de Message Outlook**.
    
6. Tapez un nom pour le fichier, cliquez sur **Enregistrer**.
    
7. Le fichier est enregistré dans le dossier partagé. Le fournisseur de transport MRXP remet le message vers votre boîte de réception dans Outlook.
    


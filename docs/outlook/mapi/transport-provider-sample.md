---
title: Exemple de fournisseur de transport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356587"
---
# <a name="transport-provider-sample"></a>Exemple de fournisseur de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cet exemple utilise des fichiers et des répertoires pour transmettre et recevoir des messages. Il implémente et enregistre un préprocesseur très simple qui ajoute une ligne de texte à chaque message sortant. L'exemple montre comment fractionner le contenu d'un message entre le format TNEF (Transport Neutral Encapsulation Format) et le texte. Il prend également en charge toutes les options de configuration (feuilles de propriétés, assistants et configuration de la programmation) et les options de message. Il ne prend pas en charge les interfaces de transport à distance. 
  
Vous pouvez télécharger cet exemple à partir d' [exemples de code MAPI (Outlook messagING API)](https://go.microsoft.com/fwlink/?LinkId=129740).
  
|||
|:-----|:-----|
|Exécutable  <br/> |mrxp32. dll  <br/> |
|Répertoire de code source:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Langue  <br/> |C++  <br/> |
|Formes  <br/> |Visual Studio 2008 à compiler pour Windows Vista, Windows Server 2008, Windows XP SP2 et Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Fonctionnalités prises en charge

Cet exemple prend en charge les fonctionnalités suivantes:
  
- Fonctionnalités de base, telles que l'envoi, la réception et l'interrogation pour les nouveaux messages.
    
- Configuration interactive et par programmation.
    
- Interface **IMAPIStatus** , à l'exception du paramètre Property. Pour plus d'informations, reportez-vous à l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . 
    
- Sécurité des threads.
    
- Journalisation des événements dans un fichier texte. Le fichier est automatiquement limité à une taille spécifiée. Toutes les sessions de transport utilisent le même fichier.
    
## <a name="unsupported-features"></a>Fonctionnalités non prises en charge

Cet exemple ne prend pas en charge la détection asynchrone des messages entrants.
  
 **Pour installer l'exemple de fournisseur de transport**
  
1. Pour télécharger l'exemple de fournisseur de transport, consultez [la rubrique téléchargement des exemples MAPI Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Recherchez le dossier dans lequel vous avez enregistré les exemples MAPI Outlook. Cliquez avec le bouton droit sur le dossier zip de **\<\> numéro de version OutlookMAPISamples** et cliquez sur **extraire tout**.
    
3. Cliquez sur **Parcourir**, sélectionnez l'emplacement où vous souhaitez enregistrer l'exemple, puis cliquez sur **extraire**.
    
4. Exécutez Visual Studio 2008.
    
5. Dans Visual Studio 2008, cliquez sur **fichier**, sur **ouvrir**, puis sur **projet/solution**.
    
6. Naviguez jusqu'à l'emplacement où vous avez enregistré l'exemple, cliquez sur **mrxp32. vcproj**, puis cliquez sur **ouvrir**.
    
7. Dans le menu **générer** , cliquez sur **Gestionnaire de configuration**.
    
8. Dans la boîte de dialogue **Gestionnaire de configuration** , accédez à la ligne **mrxp32** , puis, dans la colonne **configuration** , sélectionnez **publier**, puis cliquez sur **Fermer**.
    
9. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
10. Dans la boîte de dialogue **enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
11. Dans le dossier où vous avez enregistré l'exemple, cliquez avec le bouton droit sur le fichier de commandes d'installation, puis cliquez sur **exécuter en tant qu'administrateur**.
    
12. Dans la boîte de dialogue **contrôle de compte d'utilisateur** , cliquez sur **Continuer**.
    
    > [!NOTE]
    > **install. bat** copie le fichier. dll dans le dossier d'installation par défaut de Microsoft Office, C:\Program Files\Microsoft Office\Office12\. Si vous avez installé les produits Office à un autre emplacement, cliquez avec le bouton droit sur **install. bat** et cliquez sur **modifier**. Le fichier s'ouvre dans le bloc-notes. Remplacez le chemin d'installation par défaut par le chemin d'installation utilisé sur votre ordinateur. 
  
 **Pour configurer le fournisseur de transport dans Outlook**
  
1. Dans le menu **Outils** d'Outlook, cliquez sur **paramètres du compte**.
    
2. Dans la boîte de dialogue **paramètres du compte** , sous l'onglet **messagerie** , cliquez sur **nouveau**.
    
3. Sous **choisir le service de messagerie** , cliquez sur **autre**, sélectionnez **MRXP**, puis cliquez sur **suivant**.
    
4. Dans la boîte de dialogue **configuration du transport MRXP** , tapez le **nom complet**de l'utilisateur.
    
5. Sous **chemin d'accès à la boîte de réception (partage UNC),** entrez un chemin d'accès au dossier. Il peut également s'agir d'un chemin d'accès à un dossier local. 
    
    > [!IMPORTANT]
    > Ce chemin d'accès doit exister. 
  
6. Cliquez sur **OK**.
    
7. Dans la boîte de dialogue **Ajouter un compte de courrier** , cliquez sur **OK**. Cliquez sur **Terminer** , puis sur **Fermer**.
    
8. Pour commencer à utiliser le compte MRXP, quittez et redémarrez Outlook.
    
 **Pour utiliser l'exemple de fournisseur de transport pour envoyer un message dans Outlook**
  
1. Dans le menu **fichier** , cliquez sur **nouveau**, puis sur **message électronique**.
    
2. Dans la zone **à** , tapez le nom du destinataire au format **[MRXP:\<adresse\>]**. L'adresse est le partage UNC ou le chemin d'accès au dossier local de la boîte de réception du destinataire.
    
    > [!NOTE]
    > S'il y a deux-points ou barres obliques inverses dans l'adresse, vous devez insérer une barre oblique inverse avant chaque signe deux-points ou barre oblique inverse. Par exemple, pour envoyer un message électronique à [MRXP: C: \Mail\myDir], `[MRXP:C\:\\Mail\\myDir]`vous devez taper. 
  
    > [!IMPORTANT]
    > L'adresse du destinataire doit exister. 
  
3. Cliquez sur **compte** , puis sur **exemple de transport MRXP**.
    
4. Tapez votre message, puis cliquez sur **Envoyer**. Le message est envoyé à l'aide du fournisseur de transport MRXP.
    
 **Pour utiliser l'exemple de fournisseur de transport pour recevoir un message dans Outlook**
  
1. Dans le menu **fichier** , cliquez sur **nouveau**, puis sur **message électronique**.
    
2. Tapez votre message.
    
3. Cliquez sur le **bouton Microsoft Office**, cliquez sur **Enregistrer sous**, puis cliquez sur **Enregistrer sous** pour enregistrer le fichier dans le dossier boîte de réception que vous avez spécifié lors de l'installation. 
    
4. Dans la boîte de dialogue **Enregistrer sous** , accédez au partage UNC ou au dossier local que vous avez défini comme boîte de réception. 
    
5. Dans la liste déroulante **type de fichier** , cliquez sur **format de message Outlook**.
    
6. Tapez un nom pour le fichier, puis cliquez sur **Enregistrer**.
    
7. Le fichier est enregistré dans le dossier partagé. Le fournisseur de transport MRXP remet le message à votre boîte de réception dans Outlook.
    


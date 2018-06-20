---
title: Test des fonctionnalités, l’authentification et la configuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: Cette rubrique décrit les tests pour obtenir les fonctionnalités et les scénarios de configuration d’un compte et l’authentification d’un utilisateur pour un réseau social.
ms.openlocfilehash: ac294291e2226dbb73f822b2a641fe2bf67ce5eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787710"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Test des fonctionnalités, l’authentification et la configuration

Cette rubrique décrit les tests pour obtenir les fonctionnalités et les scénarios de configuration d’un compte et l’authentification d’un utilisateur pour un réseau social.
  
## <a name="getting-capabilities"></a>Obtention des fonctionnalités

Un fournisseur Outlook Social Connector (OSC) implémente [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)et les appels OSC **GetCapabilities** pour obtenir les fonctionnalités prises en charge par le fournisseur. Les fonctionnalités que votre fournisseur prend en charge pour votre réseau social doivent être connues au moment de la mise en œuvre et ne doivent pas dépendre d’un appel vers le réseau social en temps réel. Par exemple, les utilisateurs d’Outlook peuvent démarrer Outlook en mode hors connexion et **GetCapabilities** ne peut pas s’appuient sur la connectivité réseau à l’heure de démarrage d’Outlook. 
  
Test du fournisseur, vous devez vérifier que le paramètre de chaîne de _résultats_ renvoyé par **GetCapabilities** est conforme à l’élément **capabilities** tel que défini par le schéma XML du fournisseur OSC. Pour plus d’informations, voir [Fonctionnalités des éléments XML](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Configuration d’un compte

Lorsque l’OSC configure un compte, vous devez vérifier si l’icône de réseau social et le nom s’affichent, et que les liens hypertexte-créer un compte et mot de passe oublié apparaissent dans la boîte de dialogue de configuration de compte tel que spécifié par le fournisseur.
  
### <a name="social-network-icon-and-name"></a>Nom et l’icône de réseau social

Après avoir obtenu les fonctionnalités, l’OSC peut continuer pour obtenir l’icône et le nom du réseau social en appelant [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) et [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md). Effectuez les tests suivants pour vérifier que ces appels de méthode réussissent.
  
|**Élément à tester**|**Comportement attendu**|
|:-----|:-----|
|Icône de réseau social  <br/> | L’icône de réseau social s’affiche correctement aux emplacements suivants dans l’OSC :  <br/>  Dans la boîte de dialogue OSC pour les **Comptes de réseau Social**.  <br/>  Dans le menu déroulant lorsque vous essayez d’ajouter une personne comme un ami.  <br/>  Dans le logo lorsqu’ils suivent un ami.  <br/> <br/>**Remarque**: vous pouvez accéder à la boîte de dialogue pour les **Comptes de réseau Social** en cliquant sur l’onglet **affichage** dans Outlook, dans le groupe du **Volet personnes** , en cliquant sur le **Volet personnes**, puis en cliquant sur **Paramètres du compte**.           |
|Nom de réseau social  <br/> | Le nom de réseau social s’affiche correctement aux emplacements suivants dans l’OSC :  <br/>  Dans la boîte de dialogue OSC pour les **Comptes de réseau Social**.  <br/>  Dans le menu déroulant lorsque vous essayez d’ajouter une personne comme un ami.  <br/>  Le titre de la boîte de dialogue mot de passe lorsque vous essayez de remplacer le mot de passe.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Affichage des liens hypertexte dans la boîte de dialogue configuration

Après avoir appelé **ISocialProvider::GetCapabilities**, l’OSC utilise la valeur de l’élément **hideHyperlinks** dans le paramètre de _résultats_ afin de déterminer s’il faut afficher ou masquer la **Cliquez ici pour créer un compte** et **oublié votre le mot de passe ?** liens hypertexte dans la boîte de dialogue de configuration de compte. Vérifiez que si **hideHyperlinks** a la **valeur false**, la configuration du compte affiche ces URL.
  
### <a name="support-to-create-account"></a>Prise en charge pour créer un compte

Vérifiez que si le paramètre de _résultats_ à partir de l’appel de méthode **ISocialProvider::GetCapabilities** a l’élément **hideHyperlinks** la valeur **false** et l’élément **createAccountUrl** la valeur **true**, en cliquant sur l’URL Ouvre la page dans le navigateur web par défaut.
  
### <a name="support-for-forgotten-password"></a>Prise en charge de mot de passe oublié

Vérifiez que si le paramètre de _résultats_ à partir de l’appel de méthode **ISocialProvider::GetCapabilities** a l’élément **hideHyperlinks** la valeur **false** et l’élément **forgotPasswordUrl** la valeur **true**, en cliquant sur l’URL Ouvre la page dans le navigateur web par défaut.
  
## <a name="authenticating-users"></a>Authentification des utilisateurs

Tester les scénarios suivants, quel que soit si votre fournisseur OSC prend en charge l’authentification de base ou l’authentification basée sur les formulaires.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Ouverture de session pour la première fois.  <br/> |L’utilisateur peut se connecter au réseau social.  <br/> |
|Ouvrez une session avec un mot de passe d’une variété de caractères, y compris la ponctuation et les caractères Unicode.  <br/> |L’utilisateur peut se connecter au réseau social, indépendamment du type de caractères utilisés dans le mot de passe.  <br/> |
|La boîte de dialogue pour les **Comptes de réseau Social** affichant le nom d’utilisateur ou le code.  <br/> |Une fois que l’utilisateur a correctement connecté au réseau, boîte de dialogue de l’OSC pour les **Comptes de réseau Social** affiche le nom de l’utilisateur connecté ou le code.  <br/> |
|L’authentification échoue.  <br/> |L’OSC affiche le message d’erreur **nom d’utilisateur non valide ou le mot de passe**.  <br/> |
|Impossible de se connecter au réseau social.  <br/> |L’OSC affiche l’erreur **serveur est introuvable**.  <br/> |
|La capacité à récupérer des éléments.  <br/> |Une fois que l’utilisateur est authentifié, toutes les activités doivent être autorisées. Il n’y a aucune erreur l’obtention de données des amis ou des activités.  <br/> |
|Se connecter au réseau social après le redémarrage d’Outlook.  <br/> |Si le fournisseur OSC permet à la mise en cache du mot de passe, une fois que l’utilisateur a authentifié la première fois, l’utilisateur n’est pas par la suite invité pour les informations d’identification chaque fois que l’OSC tente d’obtenir des données à partir du réseau social.  <br/> |
   
En outre, si votre fournisseur OSC prend en charge l’authentification basée sur les formulaires, tester ainsi que le scénario suivant.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|L’obtention d’une URL à un formulaire pour l’utilisateur à se connecter à partir de l’appel [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)OSC.  <br/> |L’OSC ouvre l’URL dans le navigateur par défaut de l’utilisateur et la page Web permet à l’utilisateur d’entrer les informations d’identification pour se connecter au réseau social.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Fonctionnalités des éléments XML](capabilities-xml-elements.md)  
- [Authentification de base](basic-authentication.md) 
- [Authentification basée sur les formulaires](forms-based-authentication.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)


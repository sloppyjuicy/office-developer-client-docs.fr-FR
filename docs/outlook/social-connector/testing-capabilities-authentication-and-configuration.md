---
title: Test de fonctionnalités, authentification et configuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: Cette rubrique décrit les tests d’obtention de fonctionnalités et les scénarios de configuration d’un compte et d’authentification d’un utilisateur pour un réseau social.
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423502"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Test de fonctionnalités, authentification et configuration

Cette rubrique décrit les tests d’obtention de fonctionnalités et les scénarios de configuration d’un compte et d’authentification d’un utilisateur pour un réseau social.
  
## <a name="getting-capabilities"></a>Obtention des fonctionnalités

Un fournisseur Outlook Social Connector (OSC) implémente [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)et l’OSC appelle **GetCapabilities** pour obtenir la fonctionnalité prise en charge par le fournisseur. Les fonctionnalités que votre fournisseur prend en charge pour votre réseau social doivent être connues au moment de l’implémentation et ne doivent pas dépendre d’un appel au réseau social en temps réel. Par exemple, Outlook utilisateurs peuvent démarrer Outlook hors connexion, et **GetCapabilities** ne peut pas compter sur la connectivité réseau au moment où Outlook démarre. 
  
Lors du test du fournisseur,  vous devez vérifier que le paramètre de chaîne de résultats renvoyé par **GetCapabilities** est conforme à l’élément **capabilities** tel que défini par le schéma XML du fournisseur OSC. Pour plus d’informations, voir [Capabilities XML Elements](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Configuration d’un compte

Lorsque l’OSC configure un compte, vous devez vérifier si l’icône et le nom du réseau social sont affichés, et que les liens hypertexte créer-compte et mots de passe oubliés apparaissent dans la boîte de dialogue de configuration du compte, comme spécifié par le fournisseur.
  
### <a name="social-network-icon-and-name"></a>Icône et nom du réseau social

Après l’obtention des fonctionnalités, l’OSC peut continuer à obtenir l’icône et le nom du réseau social en appelant [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) et [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md). Pour vérifier que ces appels de méthode réussissent, faites les tests suivants.
  
|**Élément à tester**|**Comportement attendu**|
|:-----|:-----|
|Icône de réseau social  <br/> | L’icône du réseau social s’affiche correctement aux endroits suivants dans OSC :  <br/>  Dans la boîte de dialogue OSC pour les **comptes de réseau social.**  <br/>  Dans le menu déroulant, lorsque vous essayez d’ajouter une personne en tant qu’ami.  <br/>  Dans le badge lors du suivi d’un ami.  <br/> <br/>**REMARQUE**: vous pouvez accéder à la boîte de  dialogue Comptes de réseau  social en cliquant sur l’onglet Affichage dans Outlook, dans le groupe Volet Personnes, en cliquant sur Volet **Personnes,** puis sur Compte **Paramètres**.            |
|Nom du réseau social  <br/> | Le nom du réseau social s’affiche correctement aux endroits suivants dans OSC :  <br/>  Dans la boîte de dialogue OSC pour les **comptes de réseau social.**  <br/>  Dans le menu déroulant, lorsque vous essayez d’ajouter une personne en tant qu’ami.  <br/>  Titre de la boîte de dialogue de mot de passe lorsque vous tentez de modifier le mot de passe existant.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Affichage des liens hypertexte dans la boîte de dialogue de configuration

Après avoir appelé **ISocialProvider::GetCapabilities,** l’OSC utilise la valeur  de l’élément **hideHyperlinks** dans le paramètre de résultats pour déterminer s’il faut masquer ou afficher le bouton Cliquer ici pour créer un compte et vous avez oublié votre mot de passe **?** des liens hypertexte dans la boîte de dialogue de configuration du compte.  Vérifiez que si **hideHyperlinks est** **faux,** la configuration du compte affiche ces URL.
  
### <a name="support-to-create-account"></a>Prise en charge de la création d’un compte

Vérifiez que  si le paramètre de résultats de l’appel de méthode **ISocialProvider::GetCapabilities** a l’élément **hideHyperlinks** définie sur **false** et que l’élément **createAccountUrl** a la valeur **true**, le fait de cliquer sur l’URL ouvre la page dans le navigateur web par défaut.
  
### <a name="support-for-forgotten-password"></a>Prise en charge des mots de passe oubliés

Vérifiez que  si le paramètre de résultats de l’appel de méthode **ISocialProvider::GetCapabilities** a l’élément **hideHyperlinks** définie sur **false** et que l’élément **forgotPasswordUrl** a la valeur **true**, le fait de cliquer sur l’URL ouvre la page dans le navigateur web par défaut.
  
## <a name="authenticating-users"></a>Authentification des utilisateurs

Testez les scénarios suivants, que votre fournisseur OSC prend en charge l’authentification de base ou l’authentification basée sur les formulaires.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Ouverture de session pour la première fois.  <br/> |L’utilisateur peut se connecter au réseau social.  <br/> |
|Connectez-vous avec un mot de passe composé de divers caractères, y compris les caractères de ponctuation et Unicode.  <br/> |L’utilisateur peut se connecter au réseau social, indépendamment du type de caractères utilisés dans le mot de passe.  <br/> |
|Boîte de dialogue pour **les comptes de réseau social** affichant le nom d’utilisateur ou l’ID.  <br/> |Une fois que l’utilisateur s’est connecté au réseau,  la boîte de dialogue des comptes de réseau social de l’OSC affiche le nom d’utilisateur ou l’ID connecté.  <br/> |
|L’authentification échoue.  <br/> |L’OSC affiche l’erreur **Nom d’utilisateur ou mot de passe non valide.**  <br/> |
|Impossible de se connecter au réseau social.  <br/> |L’OSC affiche le serveur d’erreur **in retrouve.**  <br/> |
|Possibilité de récupérer des éléments.  <br/> |Une fois que l’utilisateur s’est authentifié, toutes les activités doivent être autorisées. Il n’y a aucune erreur lors de l’obtention des données ou des activités des amis.  <br/> |
|Connectez-vous au réseau social après le redémarrage Outlook.  <br/> |Si le fournisseur OSC autorise la mise en cache du mot de passe, une fois que l’utilisateur s’est authentifié pour la première fois, l’utilisateur n’est pas invité à entrer ses informations d’identification chaque fois que l’OSC tente d’obtenir des données à partir du réseau social.  <br/> |
   
En outre, si votre fournisseur OSC prend en charge l’authentification basée sur les formulaires, testez également le scénario suivant.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|L’OSC obtenant une URL vers un formulaire pour que l’utilisateur se connecte à partir de l’appel [de ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md).  <br/> |L’OSC ouvre l’URL dans le navigateur par défaut de l’utilisateur, et la page web permet à l’utilisateur d’entrer ses informations d’identification pour se connecter au réseau social.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Éléments XML de fonctionnalités](capabilities-xml-elements.md)  
- [Authentification de base](basic-authentication.md) 
- [Authentification basée sur les formulaires](forms-based-authentication.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)


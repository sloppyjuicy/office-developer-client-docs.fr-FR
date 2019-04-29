---
title: Test de fonctionnalités, authentification et configuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: Cette rubrique décrit les tests d'obtention de fonctionnalités, ainsi que les scénarios de configuration d'un compte et d'authentification d'un utilisateur pour un réseau social.
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423502"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Test de fonctionnalités, authentification et configuration

Cette rubrique décrit les tests d'obtention de fonctionnalités, ainsi que les scénarios de configuration d'un compte et d'authentification d'un utilisateur pour un réseau social.
  
## <a name="getting-capabilities"></a>Obtention de fonctionnalités

Un fournisseur Outlook Social Connector (OSC) implémente [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md)et le OSC appelle **GetCapabilities** pour obtenir les fonctionnalités prises en charge par le fournisseur. Les fonctionnalités prises en charge par votre fournisseur pour votre réseau social doivent être connues au niveau de l'implémentation et ne doivent pas dépendre d'un appel au réseau social en temps réel. Par exemple, les utilisateurs d'Outlook peuvent démarrer Outlook en mode hors connexion et **GetCapabilities** ne peuvent pas utiliser la connectivité réseau au moment du démarrage d'Outlook. 
  
Lors du test du fournisseur, vous devez vérifier que le paramètre de chaîne de _résultats_ renvoyé par **GetCapabilities** est conforme à l'élément **Capabilities** tel que défini par le schéma XML du fournisseur OSC. Pour plus d'informations, consultez la rubrique [Capabilities XML Elements](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Configuration d'un compte

Lorsque le OSC configure un compte, vous devez vérifier si l'icône et le nom du réseau social sont affichés, et si les liens hypertexte de création de compte et de mot de passe oublié apparaissent dans la boîte de dialogue Configuration du compte, comme indiqué par le fournisseur.
  
### <a name="social-network-icon-and-name"></a>Nom et icône du réseau social

Après avoir obtenu les fonctionnalités, OSC peut accéder à l'icône et au nom du réseau social en appelant [ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) et [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md). Effectuez les tests suivants pour vérifier que ces appels de méthode réussissent.
  
|**Élément à tester**|**Comportement attendu**|
|:-----|:-----|
|Icône de réseau social  <br/> | L'icône du réseau social s'affiche correctement aux emplacements suivants dans le OSC:  <br/>  Dans la boîte de dialogue OSC pour les **comptes de réseau social**.  <br/>  Dans le menu déroulant, lorsque vous tentez d'ajouter une personne en tant qu'ami.  <br/>  Dans le badge à la suite d'un ami.  <br/> <br/>**Remarque**: vous pouvez accéder à la boîte de dialogue des **comptes de réseau social** en cliquant sur l'onglet **affichage** dans Outlook, dans le groupe **volet personnes** , en cliquant sur **volet contacts**, puis en cliquant sur **paramètres du compte**.           |
|Nom du réseau social  <br/> | Le nom du réseau social est correctement affiché aux emplacements suivants dans le OSC:  <br/>  Dans la boîte de dialogue OSC pour les **comptes de réseau social**.  <br/>  Dans le menu déroulant, lorsque vous tentez d'ajouter une personne en tant qu'ami.  <br/>  Comme titre de la boîte de dialogue mot de passe lorsque vous tentez de modifier le mot de passe existant.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Affichage de liens hypertexte dans la boîte de dialogue de configuration

Après avoir appelé **ISocialProvider:: GetCapabilities**, OSC utilise la valeur de l'élément **hideHyperlinks** dans le paramètre _results_ pour déterminer s'il faut masquer ou afficher le **lien cliquez ici pour créer un compte** et **oublier votre mot de passe?** liens hypertexte dans la boîte de dialogue Configuration du compte. Vérifiez que si **hideHyperlinks** a la **valeur false**, la configuration du compte affiche ces URL.
  
### <a name="support-to-create-account"></a>Prise en charge de la création d'un compte

Vérifiez que si le __ paramètre Results de l'appel de méthode **ISocialProvider:: GetCapabilities** a l'élément **hideHyperlinks** défini sur **false** et que l'élément **createAccountUrl** a la valeur **true**, le fait de cliquer sur l'URL ouvre la page dans le navigateur Web par défaut.
  
### <a name="support-for-forgotten-password"></a>Prise en charge du mot de passe oublié

Vérifiez que si le __ paramètre Results de l'appel de méthode **ISocialProvider:: GetCapabilities** a l'élément **hideHyperlinks** défini sur **false** et que l'élément **forgotPasswordUrl** a la valeur **true**, le fait de cliquer sur l'URL ouvre la page dans le navigateur Web par défaut.
  
## <a name="authenticating-users"></a>Authentification des utilisateurs

Testez les scénarios suivants, que votre fournisseur OSC prenne en charge l'authentification de base ou l'authentification basée sur les formulaires.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Connexion pour la première fois.  <br/> |L'utilisateur peut se connecter au réseau social.  <br/> |
|Ouverture de session avec un mot de passe composé de plusieurs caractères, y compris la ponctuation et les caractères Unicode.  <br/> |L'utilisateur peut se connecter au réseau social, indépendamment du type de caractères utilisés dans le mot de passe.  <br/> |
|La boîte de dialogue pour les **comptes de réseau social** affichant le nom d'utilisateur ou l'ID.  <br/> |Une fois que l'utilisateur a réussi à se connecter au réseau, la boîte de dialogue de l'OSC pour les **comptes de réseau social** affiche le nom ou l'ID de l'utilisateur connecté.  <br/> |
|L'authentification échoue.  <br/> |Le OSC affiche le **nom d'utilisateur ou le mot de passe non valide**.  <br/> |
|Impossible de se connecter au réseau social.  <br/> |Le OSC affiche le serveur d'erreurs **est**introuvable.  <br/> |
|Possibilité de récupérer des éléments.  <br/> |Une fois que l'utilisateur est authentifié, toutes les activités doivent être autorisées. Il n'y a aucune erreur lors de l'obtention des données ou des activités des amis.  <br/> |
|Connexion au réseau social après le redémarrage d'Outlook.  <br/> |Si le fournisseur OSC autorise la mise en cache du mot de passe, après la première authentification de l'utilisateur, l'utilisateur n'est pas invité à fournir des informations d'identification chaque fois que OSC tente d'obtenir des données à partir du réseau social.  <br/> |
   
En outre, si votre fournisseur OSC prend en charge l'authentification basée sur les formulaires, testez également le scénario suivant.
  
|**Scénario**|**Comportement attendu**|
|:-----|:-----|
|Le OSC Obtient une URL vers un formulaire pour que l'utilisateur se connecte à partir de [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md).  <br/> |Le OSC ouvre l'URL dans le navigateur par défaut de l'utilisateur et la page Web permet à l'utilisateur d'entrer des informations d'identification pour se connecter au réseau social.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Éléments XML des fonctionnalités](capabilities-xml-elements.md)  
- [Authentification de base](basic-authentication.md) 
- [Authentification basée sur les formulaires](forms-based-authentication.md)
- [Prise en main de la publication d'un fournisseur OSC](getting-ready-to-release-an-osc-provider.md)


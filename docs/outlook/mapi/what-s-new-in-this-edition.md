---
title: Nouveautés dans cette édition
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 7325c42fe7e9c1e043609d5503a3782522f76188
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590056"
---
# <a name="whats-new-in-this-edition"></a>Nouveautés dans cette édition

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La référence Microsoft Outlook 2013 MAPI a été mis à jour pour inclure la documentation pour différentes nouvelles fonctionnalités. 
  
## <a name="new-content"></a>Nouveau contenu

Le contenu a été ajouté pour les fonctionnalités suivantes :
  
- La rubrique [Mise en route avec la référence MAPI Outlook 2013](getting-started-with-the-outlook-mapi-reference.md) a été mis à jour pour faire référence à des informations complètes sur la programmation des modèles pour vos fonctionnalités d’Outlook et MAPI pour vous aider à identifier les API et technologies plus souvent adapté à vos besoins. Des liens vers l’Article de référence technique ont également été modifiées dans les rubriques suivantes : 
    
  - [Référence MAPI Outlook](outlook-mapi-reference.md)
    
  - [Vue d’ensemble de la référence MAPI Outlook](outlook-mapi-reference-overview.md)
    
- **Exemple de fournisseur de magasin de message**: le code [Exemple renvoyé à la ligne de fournisseur de magasin PST](message-store-provider-sample.md) maintenant a été révisé pour reconnaître et prendre en charge Outlook 2013. Pour plus d’informations, voir contenu précédemment révisée dans cette rubrique. 
    
- **Flux de saisie semi-automatique**— la rubrique [cache du surnom dans](nickname-cache.md) , anciennement le **Format de fichier Nk2**, a été mis à jour pour refléter les modifications apportées dans Outlook 2013, ainsi que Outlook 2010. Les rubriques suivantes ont été révisées maintenant pour fournir des informations sur les instructions de développeur de format de fichier .nk2 pour Microsoft Outlook 2003/Microsoft Office Outlook 2007 et l’analyse des fichiers binaires. Pour plus d’informations, voir contenu précédemment révisée dans cette rubrique.
    
  - [Profils MAPI](mapi-profiles.md)
    
  - [Cache de surnoms](nickname-cache.md)
    
  - [Flux de saisie semi-automatique](autocomplete-stream.md)
    
- **Interfaces**-la rubrique [IAddrBook::OpenEntry](iaddrbook-openentry.md) documents d’une méthode d’ouverture d’une entrée de carnet d’adresses et qui retourne un pointeur vers l’interface permettant d’y accéder. Il contenait auparavant un indicateur dans le paramètre *ulFlags* , **MAPI_GAL_ONLY**, qui peut être utilisé pour ouvrir la liste (globale), uniquement et a été modifiée pour inclure sa définition.
    
- **Propriétés**— la **PR_CONVERSATION_KEY** nommé rubrique de la propriété ([Propriété canonique PidTagConversationKey](pidtagconversationkey-canonical-property.md)) a été ajoutée et se rapporte à **IPM. MessageManager** uniquement les messages dans Outlook MAPI. Les rubriques suivantes concernant la documentation de flux de Transport-Neutral Encapsulation Format (TNEF) et ont été révisées : 
    
  - [Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Mappage d’attributs TNEF aux propriétés MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID et attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Contenu précédemment révisé

Le contenu a été ajouté dans les versions précédentes de la référence MAPI Outlook pour les fonctionnalités suivantes :
  
- Permet à Microsoft Outlook 2013 pour les scénarios de déploiement non traditionnels tels que côte à côte et Click-to-Run. Ces scénarios peuvent compliquer la logique utilisée pour charger la bibliothèque appropriée de MAPI. Les développeurs MAPI est maintenant ont la possibilité de liaison explicite fonctions MAPI et peuvent choisir pour une liaison explicite vers le stub MAPI du client MAPI par défaut (par exemple, une Msmapi32.dll d’Outlook) sans passer par la bibliothèque MAPI et le stub MAPI Windows. Pour plus d’informations sur la liaison explicite par rapport à la liaison implicite, voir [lien vers des fonctions MAPI](how-to-link-to-mapi-functions.md). La **Bibliothèque de Stub MAPI**, publié sur le site Web [CodePlex](http://mapistublibrary.codeplex.com/) , fournit une solution de remplacement dans le désordre pour Mapi32.lib qui prend en charge la création d’applications MAPI 32 bits et 64 bits. 
    
- **Prise en charge de 64 bits de Microsoft Outlook**, les rubriques de référence pour les éléments d’API applicables ont été mis à jour pour correspondre aux nouveaux fichiers d’en-tête qui prennent en charge Outlook 64 bits. Ces fichiers d’en-tête sont disponibles en téléchargement à [Outlook 2010 : fichiers d’en-tête MAPI](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Un nouvel exemple de code a été fourni dans [vérifier la Version d’Outlook](how-to-check-the-version-of-outlook.md) pour montrer comment vérifier si la version installée d’Outlook est de 64 bits de Microsoft Outlook 2010 et a été modifiée pour Outlook 2013. Si votre application de MAPI 32 bits existante sur le point d’être en cours d’exécution sur un système d’exploitation 64 bits avec Outlook 64 bits est installé, vous devrez reconstruire votre application 32 bits comme une application 64 bits. Pour plus d’informations sur la prise en charge MAPI pour Outlook 64 bits, consultez [Création d’Applications MAPI sur les plateformes 32 bits et 64 bits](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Exemple de fournisseur de magasin de message**: le [Fournisseur de banque PST encapsulé exemple](message-store-provider-sample.md) avait été précédemment mis à jour pour prendre en charge l’architecture 64 bits. Rubrique de [l’initialisation d’un fournisseur de magasins PST entourées](initializing-a-wrapped-pst-store-provider.md) de l’exemple maintenant a été développé pour fournir des informations sur les « Wrapped PST et les chemins d’accès Unicode. » 
    
- **Flux de saisie semi-automatique**— la rubrique [cache du surnom dans](nickname-cache.md) , anciennement le **Format de fichier Nk2**, a été mis à jour pour refléter les modifications apportées dans Outlook 2013, ainsi que Outlook 2010. Des informations telles que la liste de saisie semi-automatique, qui est la liste de noms qui s’affiche dans la **à**, **Cc**, **Cci modifier** pendant un utilisateur compose un message électronique, sont désormais enregistrées dans le [flux de saisie semi-automatique](autocomplete-stream.md) d’un message sur l’ordinateur local au lieu de l’enregistrer dans un fichier comme dans Outlook 2007. 
    
  - Interaction avec le flux de saisie semi-automatique
    
  - Chargement du flux de saisie semi-automatique
    
  - L’enregistrement du flux de saisie semi-automatique
    
- **Prise en charge de l’arrêt rapide des clients MAPI**— clients MAPI peuvent désormais initier un arrêt rapide et le sous-système MAPI avertir chargés fournisseurs afin de réduire la perte de données à partir de l’arrêt rapide. Interfaces supplémentaires ont été ajoutées pour le client et le fournisseur prendre en charge l’arrêt rapide. Pour plus d’informations sur l’arrêt rapide, voir [L’arrêt du Client MAPI](client-shutdown-in-mapi.md).
    
- **Structure de flux de données pour les définitions de champ pour un élément Outlook**, la Documentation d’un flux binaire pour la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) a été ajoutée. Cette propriété spécifie les définitions de tous les champs personnalisés et les paramètres de liaison de données pour les champs intégrés d’un élément Outlook. 
    
- **Remplacer magasin personnel**— les interfaces suivantes et leurs méthodes respectives ont été ajoutés pour prendre en charge la substitution de la stratégie de dossiers personnels (PST) de fichier magasin de fournisseurs **PSTDisableGrow** : 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **À l’aide de plusieurs comptes Exchange**— Documentation pour l' [API de carnet d’adresses MAPI](using-multiple-exchange-accounts.md) a été ajoutée. Cette API a été améliorée pour prendre en charge plusieurs comptes Exchange dans Microsoft Outlook 2010 et inclut désormais Microsoft Outlook 2013. R�soudre les adresses correctement avec plusieurs comptes Exchange, utilisez les nouvelles fonctions qui utilisent un contexte de compte afin que les appels vers le carnet d'adresses rechercher le compte Exchange appropri�. 
    
- **Formats de fichiers MAPI**— les informations de configuration MAPI a été développées pour expliquer comment vous pouvez utiliser des chemins d’accès dans [les Services d’inscription et fournisseurs de services de MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propriétés**: les propriétés balisées suivantes ont été ajoutées en plus de la documentation pour 38 autres balisé des propriétés et nommé propriétés avaient déjà été ajoutées :
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes MAPI**— consolidée [Constantes MAPI](mapi-constants.md) ont été développés. Dans les versions précédentes, ils ont été distribuées en un nombre de rubriques, mais sont désormais rassemblées dans une seule rubrique pour les rendre plus faciles à découvrir et à utiliser. Ils ont également été développés pour fournir une couverture plus large, y compris les sections suivantes : 
    
  - Définitions de carnet d’adresses Exchange et les Codes d’erreur de banque de messages
    
  - Définitions de boîte aux lettres du serveur Exchange mis en cache en Mode Quotas
    
## <a name="see-also"></a>Voir aussi



[Mise en route avec la référence de MAPI pour Outlook 2013](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](http://mapistublibrary.codeplex.com/)


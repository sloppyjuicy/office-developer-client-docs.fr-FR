---
title: Nouveautés de cette édition
manager: soliver
ms.date: 2/09/2020
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Last modified: February 09, 2020'
ms.openlocfilehash: 3a3d38d83311b63686a2379c3321194e538ff840
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061327"
---
# <a name="whats-new-in-this-edition"></a>Nouveautés de cette édition

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La référence MAPI Outlook Microsoft a été mise à jour pour inclure la documentation de diverses nouvelles fonctionnalités. 
  
## <a name="new-content"></a>Nouveau contenu

Le contenu a été ajouté pour les fonctionnalités suivantes :
  
- La rubrique Getting [Started with the Outlook 2013 MAPI Reference has](getting-started-with-the-outlook-mapi-reference.md) been updated to reference comprehensive information about programming models for your Outlook and MAPI functionality to help you identify the APIs and technologies that are most appropriate for your needs. Les liens vers l’article technique référencé ont également été révisés dans les rubriques suivantes : 
    
  - [Référence MAPI Outlook](outlook-mapi-reference.md)
    
  - [Vue d'ensemble de r�f�rence de MAPI Outlook 2013](outlook-mapi-reference-overview.md)
    
- **Exemple de fournisseur de** magasins de messages — L’exemple de code de fournisseur de magasins [PST wrapped](message-store-provider-sample.md) a été révisé pour reconnaître et prendre en charge Outlook 2013. Pour plus d’informations, voir Contenu révisé précédemment dans cette rubrique. 
    
- **Autocomplete Stream**—The [Nickname cache](nickname-cache.md) topic, formerly the **Nk2 File Format**, had been updated to reflect changes in Outlook 2013 as well as Outlook 2010. Les rubriques suivantes ont été révisées pour fournir des informations sur les instructions de développement de format de fichier .nk2 pour Microsoft Outlook 2003/Microsoft Office Outlook 2007 et l’examen des fichiers binaires. Pour plus d’informations, voir Contenu révisé précédemment dans cette rubrique.
    
  - [Profils MAPI](mapi-profiles.md)
    
  - [Cache de surnoms](nickname-cache.md)
    
  - [Autocomplete Stream](autocomplete-stream.md)
    
- **Interfaces**-The [IAddrBook::OpenEntry](iaddrbook-openentry.md) topic documents a method of opening an address book entry and returning a pointer to the interface used to access it. Il contenait précédemment un indicateur dans le paramètre  *ulFlags,* **MAPI_GAL_ONLY**, qui pouvait être utilisé pour ouvrir uniquement la liste d’adresses globale (LAG) et a été révisé pour inclure sa définition.
    
- **Propriétés** **: PR_CONVERSATION_KEY** propriété nommée ( propriété canonique [PidTagConversationKey](pidtagconversationkey-canonical-property.md)) a été ajoutée et est liée à **IPM. Messages MessageManager** dans Outlook MAPI uniquement. Les rubriques suivantes relatives à ce format et à la documentation Transport-Neutral flux TNEF (Encapsulation Format) ont été révisées : 
    
  - [Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Mappage des attributs TNEF aux propriétés MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID et attParentID](attconversationid-and-attparentid.md)
  
## <a name="mapi-initialization-monitor"></a>Moniteur d’initialisation MAPI  

- Parfois, une application qui utilise MAPI peut vouloir savoir quand l’initialisation est terminée. Par exemple, il a plusieurs threads qui pourraient initialiser MAPI, ou en réponse à l’initialisation de MAPI l’application souhaiterait effectuer un travail, mais ne souhaite pas toujours faire tourner la pile MAPI.  Le moniteur d’initialisation fournit cette fonctionnalité via une fonction (exportée à partir de OLMAPI32.DLL) et quelques interfaces simples décrites ci-dessous. 

### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor) 

- Il s’agit du point d’entrée exporté à partir de OLMAPI32.DLL cela permet à l’appelant de récupérer une interface pour interroger l’état d’initialisation actuel, configurer un rappel pour l’achèvement de l’initialisation ou bloquer le thread actuel jusqu’à ce qu’il soit terminé.  L’objet renvoyé à partir de cette API est réutilisable et thread-safe et peut être appelé à partir de n’importe quel thread, pas seulement du thread qui l’a récupéré.  En outre, contrairement aux autres objets exposés à partir de MAPI, cet objet est valide tant que la DLL est chargée, il peut être ré-utilisé entre les sessions d’initialisation et peut être utilisé avant ou après l’appel de MAPIInitialize. Renvoie le succès ou l’échec via un HRESULT standard COM et affecte un paramètre de sortie à une instance de IMAPIInitMonitor. 

### <a name="interface-imapiinitmonitor"></a>Interface : IMAPIInitMonitor 

**IFACEMETHODIMP_(BOOL) IsInitialized()**
- Renvoie l’état actuel de l’initialisation MAPI 

**IFACEMETHODIMP Wait(DWORD timeout)**
- Lance un appel BLOCKING sur ce thread, qui retourne soit lorsque le nombre de millisecondes spécifié est écoulé, soit que MAPI a été initialisé.  INFINITE peut être utilisé pour une attente infinie. 

**IFACEMETHODIMP BeginWait(DWORD timeout, IMAPIWaitResult ppResult)**
- Démarrez une attente pour l’initialisation de MAPI ou le nombre spécifié de millisecondes qui s’écoulént.   Cette commande retourne une interface IMAPIWaitResult qui doit avoir appelé « End » afin de commencer l’attente.  Cela permet à l’appelant de contrôler quel thread est bloqué pendant que nous sommes en attente. 

### <a name="interface-imapiwaitresult"></a>Interface IMAPIWaitResult
**Remplacement IFACEMETHODIMP End()**
- Appelé pour lancer l’attente bloquante sur le thread où il est appelé, il n’est pas nécessaire qu’il s’agit du même thread que celui appelé « BeginWait ». 

    
## <a name="previously-revised-content"></a>Contenu révisé précédemment

Le contenu a été ajouté dans les versions précédentes de Outlook référence MAPI pour les fonctionnalités suivantes :
  
- Microsoft Outlook 2013 permet des scénarios de déploiement non traditionnels tels que côte à côte et « Exécuter en un clic ». Ces scénarios peuvent compliquer la logique utilisée pour charger la bibliothèque MAPI appropriée. Les développeurs MAPI ont désormais la possibilité de lier explicitement des fonctions MAPI et peuvent choisir de créer un lien explicite vers le stub MAPI du client MAPI par défaut (par exemple, Msmapi32.dll de Outlook) sans passer par la bibliothèque MAPI et le stub MAPI Windows. Pour plus d’informations sur la liaison explicite par rapport à la liaison implicite, voir Lien vers les [fonctions MAPI.](how-to-link-to-mapi-functions.md) La bibliothèque **Stub MAPI,** publiée sur le site web [CodePlex,](https://mapistublibrary.codeplex.com/) fournit un remplacement de mapi32.lib qui prend en charge la création d’applications MAPI 32 bits et 64 bits. 
    
- Prise en charge de **Microsoft Outlook 64 bits**: les rubriques de référence pour les éléments d’API applicables ont été mises à jour pour correspondre aux nouveaux fichiers d’en-tête qui 64 bits Outlook. Ces fichiers d’en-tête sont disponibles en téléchargement [Outlook 2010 : fichiers d’en-tête MAPI.](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1) Un nouvel exemple de code a été fourni dans Vérifier la version de [Outlook](how-to-check-the-version-of-outlook.md) pour montrer comment vérifier si la version installée de Outlook est en Microsoft Outlook 2010 64 bits et a été révisée pour Outlook 2013. Si votre application MAPI 32 bits existante s’exécute sur un système d’exploitation 64 bits avec des Outlook 64 bits installées, vous devez reconstruire votre application 32 bits en tant qu’application 64 bits. Pour plus d’informations sur la prise en charge de MAPI pour les Outlook 64 [bits, voir Building MAPI Applications on 32-Bit and 64-Bit Platforms](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Exemple de fournisseur de magasins de** messages — L’exemple de fournisseur de magasins [PST Wrapped](message-store-provider-sample.md) a été précédemment mis à jour pour prendre en charge l’architecture 64 bits. La rubrique Initialisation d’un fournisseur de magasins [PST Wrapped a](initializing-a-wrapped-pst-store-provider.md) été étendue pour fournir des informations sur les chemins d’accès PST Wrapped et Unicode. 
    
- **Flux de** mise à jour automatique — La rubrique cache [de](nickname-cache.md) surnoms, anciennement format de fichier **Nk2,** a été mise à jour pour refléter les modifications apportées à Outlook 2013 et Outlook 2010. Les informations telles que la liste de la mise à jour automatique, qui est la liste des noms qui s’affichent [](autocomplete-stream.md) dans les zones d’édition **À,** **Cc** et **Cci** pendant qu’un utilisateur compose un e-mail, sont désormais enregistrées dans le flux de mise à jour automatique d’un message sur l’ordinateur local au lieu de l’enregistrer dans un fichier comme dans Outlook 2007. 
    
  - Interaction avec le flux decomplet automatique
    
  - Chargement du flux de la mise àcomplet automatique
    
  - Enregistrement du flux de la mise àcomplet automatique
    
- Prise en charge de l’arrêt rapide pour les **clients MAPI**: les clients MAPI peuvent désormais lancer un arrêt rapide et faire en cas d’arrêt rapide des fournisseurs chargés par le sous-système MAPI afin de minimiser la perte de données suite à l’arrêt rapide. Des interfaces supplémentaires ont été ajoutées pour le client et le fournisseur afin de prendre en charge l’arrêt rapide. Pour plus d’informations sur l’arrêt rapide, voir [l’arrêt du client dans MAPI.](client-shutdown-in-mapi.md)
    
- **Structure de flux pour les définitions** de champ pour un élément Outlook : la documentation d’un flux binaire pour la [propriété PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) a été ajoutée. Cette propriété spécifie les définitions de tous les champs personnalisés et les paramètres de liaison de données pour les champs intégrés d’Outlook élément. 
    
- **Remplacement de** magasin personnel — Les interfaces suivantes et leurs méthodes respectives ont été ajoutées pour prendre en charge le remplacement de la stratégie PST des fournisseurs de magasins de dossiers personnels **PSTDisableGrow** : 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Utilisation de plusieurs Exchange :** la documentation de l’API de carnet d’adresses [MAPI](using-multiple-exchange-accounts.md) a été ajoutée. Cette API a été améliorée pour prendre en charge plusieurs comptes Exchange dans Microsoft Outlook 2010 et inclut désormais Microsoft Outlook 2013. R�soudre les adresses correctement avec plusieurs comptes Exchange, utilisez les nouvelles fonctions qui utilisent un contexte de compte afin que les appels vers le carnet d'adresses rechercher le compte Exchange appropri�. 
    
- **Formats** de fichiers MAPI : les informations de configuration MAPI ont été étendues pour expliquer comment vous pouvez utiliser les chemins d’accès dans [Registering Services and Service Providers dans MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propriétés**: les propriétés marquées suivantes ont été ajoutées en plus de la documentation relative à 38 autres propriétés marquées et aux propriétés nommées précédemment ajoutées :
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes MAPI**— Les [constantes MAPI consolidées](mapi-constants.md) ont été étendues. Dans les versions précédentes, elles étaient distribuées dans un certain nombre de rubriques, mais elles sont désormais collectées dans une seule rubrique pour les rendre plus faciles à découvrir et à utiliser. Ils ont également été étendus pour fournir une couverture plus étendue, y compris les sections suivantes : 
    
  - Définitions des codes d Exchange de carnet d’adresses et de magasin de messages
    
  - Définitions des quotas Exchange Server en mode mis en cache de boîtes aux lettres
    
## <a name="see-also"></a>Voir aussi



[Mise en route avec la référence de MAPI pour Outlook 2013](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)


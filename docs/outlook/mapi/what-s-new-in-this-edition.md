---
title: Nouveautés de cette édition
manager: soliver
ms.date: 2/09/2020
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Dernière modification : 9 février 2020'
ms.openlocfilehash: 29e73a520a82ab12eb35bbe9aa4d281ca75a5a7d
ms.sourcegitcommit: 600f0dc552b725f98f3354d42feefc39be9c354c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2022
ms.locfileid: "66577321"
---
# <a name="whats-new-in-this-edition"></a>Nouveautés de cette édition

**S’applique à** : Outlook 2013 | Outlook 2016
  
La référence MAPI Microsoft Outlook a été mise à jour pour inclure la documentation de différentes nouvelles fonctionnalités.
  
## <a name="new-content"></a>Nouveau contenu

Le contenu a été ajouté pour les fonctionnalités suivantes :
  
- La rubrique [Prise en main avec la référence MAPI Outlook 2013](getting-started-with-the-outlook-mapi-reference.md) a été mise à jour pour référencer des informations complètes sur les modèles de programmation pour vos fonctionnalités Outlook et MAPI afin de vous aider à identifier les API et technologies les plus adaptées à vos besoins. Les liens vers l’article technique référencé ont également été révisés dans les rubriques suivantes :

  - [Référence MAPI Outlook](outlook-mapi-reference.md)
  - [Vue d'ensemble de r�f�rence de MAPI Outlook 2013](outlook-mapi-reference-overview.md)

- **Exemple de fournisseur de magasin** de messages : l’exemple de code du [fournisseur du magasin PST encapsulé](message-store-provider-sample.md) a été modifié pour reconnaître et prendre en charge Outlook 2013. Pour plus d’informations, consultez contenu précédemment révisé dans cette rubrique.

- **Flux de saisie semi-automatique** : la rubrique du [cache de surnoms](nickname-cache.md) , anciennement le **format de fichier Nk2**, a été mise à jour pour refléter les modifications apportées à Outlook 2013 et Outlook 2010. Les rubriques suivantes ont été révisées pour fournir des informations sur les instructions du développeur de format de fichier .nk2 pour Microsoft Outlook 2003/Microsoft Office Outlook 2007 et l’analyse des fichiers binaires. Pour plus d’informations, consultez contenu précédemment révisé dans cette rubrique.

  - [Profils MAPI](mapi-profiles.md)
  - [Cache de surnoms](nickname-cache.md)
  - [Flux de saisie semi-automatique](autocomplete-stream.md)

- **Interfaces-La** rubrique [IAddrBook::OpenEntry](iaddrbook-openentry.md) documente une méthode permettant d’ouvrir une entrée de carnet d’adresses et de renvoyer un pointeur vers l’interface utilisée pour y accéder. Il contenait auparavant un indicateur dans le paramètre *ulFlags* , **MAPI_GAL_ONLY**, qui pouvait être utilisé pour ouvrir la liste d’adresses globale (GAL), uniquement, et a été révisé pour inclure sa définition.

- **Propriétés** : la rubrique **PR_CONVERSATION_KEY** propriété nommée ([propriété canonique PidTagConversationKey](pidtagconversationkey-canonical-property.md)) a été ajoutée et se rapporte à **IPM. Messages MessageManager** uniquement dans Outlook MAPI. Les rubriques suivantes relatives à celui-ci et à la documentation de flux TNEF (Transport-Neutral Encapsulation Format) ont été révisées :

  - [Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  - [Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)
  - [Mappage des attributs TNEF aux propriétés MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
  - [attConversationID et attParentID](attconversationid-and-attparentid.md)
  
## <a name="mapi-initialization-monitor"></a>Moniteur d’initialisation MAPI  

- Il arrive qu’une application qui consomme MAPI souhaite savoir quand l’initialisation est terminée. Par exemple, il a plusieurs threads qui pourraient initialiser MAPI, ou en réponse à l’initialisation de MAPI, l’application souhaite effectuer un travail, mais ne veut pas toujours faire tourner la pile MAPI.  Le moniteur d’initialisation fournit cette fonctionnalité via une fonction (exportée à partir de OLMAPI32.DLL) et quelques interfaces simples décrites ci-dessous.

### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)

- Il s’agit d’un point d’entrée exporté à partir de OLMAPI32.DLL cela permet à l’appelant de récupérer une interface pour interroger l’état d’initialisation actuel, configurer un rappel pour l’achèvement de l’initialisation ou bloquer le thread actuel jusqu’à ce qu’il soit terminé.  L’objet retourné à partir de cette API est réutilisable et thread-safe et peut être appelé à partir de n’importe quel thread, et pas seulement du thread qui l’a récupéré.  En outre, contrairement à d’autres objets exposés à partir de MAPI, cet objet est valide tant que la DLL est chargée, il peut être réutilisé dans les sessions d’initialisation et peut être consommé avant ou après l’appel de MAPIInitialize. Retourne la réussite ou l’échec par le biais d’un HRESULT standard COM et affecte un paramètre out à une instance d’IMAPIInitMonitor.

### <a name="interface-imapiinitmonitor"></a>Interface : IMAPIInitMonitor

**IFACEMETHODIMP_(BOOL) IsInitialized()**

- Retourne l’état actuel de l’initialisation MAPI

**IFACEMETHODIMP Wait(DWORD timeout)**

- Lance un appel BLOCKING sur ce thread, qui retourne soit lorsque le nombre spécifié de millisecondes est écoulé, soit que MAPI a été initialisé.  INFINITE peut être utilisé pour une attente infinie.

**IFACEMETHODIMP BeginWait(DWORD timeout, IMAPIWaitResult ppResult)**

- Démarrez une attente pour l’initialisation MAPI ou le nombre spécifié de millisecondes à s’écouler.   Cette opération retourne une interface IMAPIWaitResult qui doit avoir « End » appelée dans l’ordre de début de l’attente.  Cela permet à l’appelant de contrôler quel thread est bloqué pendant que nous attendons.

### <a name="interface-imapiwaitresult"></a>Interface IMAPIWaitResult

**Remplacement de IFACEMETHODIMP End()**

- Appelé pour lancer l’attente de blocage sur le thread où il est appelé, n’a pas besoin d’être le même thread que celui appelé « BeginWait ».

## <a name="previously-revised-content"></a>Contenu précédemment révisé

Le contenu a été ajouté dans les versions précédentes de la référence MAPI Outlook pour les fonctionnalités suivantes :
  
- Microsoft Outlook 2013 permet des scénarios de déploiement non traditionnels, tels que côte à côte et Démarrer en un clic. Ces scénarios peuvent compliquer la logique utilisée pour charger la bibliothèque MAPI appropriée. Les développeurs MAPI peuvent désormais établir une liaison explicite aux fonctions MAPI et choisir de créer un lien explicite vers le stub MAPI du client MAPI par défaut (par exemple, Msmapi32.dll d’Outlook) sans passer par la bibliothèque MAPI et le stub MapI Windows. Pour plus d’informations sur la liaison explicite par rapport à la liaison implicite, consultez [Lien vers des fonctions MAPI](how-to-link-to-mapi-functions.md).
<!-- - The **MAPI Stub Library**, posted on the [CodePlex](https://mapistublibrary.codeplex.com/) website, provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications. -->

- **Prise en charge de Microsoft Outlook 64 bits** : les rubriques de référence pour les éléments d’API applicables ont été mises à jour pour correspondre aux nouveaux fichiers d’en-tête qui prennent en charge Outlook 64 bits. Ces fichiers d’en-tête sont disponibles en téléchargement dans [Outlook 2010 : Fichiers d’en-tête MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Un nouvel exemple de code a été fourni dans [Vérifier la version d’Outlook](how-to-check-the-version-of-outlook.md) pour montrer comment vérifier si la version installée d’Outlook est 64 bits Microsoft Outlook 2010 et a été révisée pour Outlook 2013. Si votre application MAPI 32 bits existante va s’exécuter sur un système d’exploitation 64 bits avec Outlook 64 bits installé, vous devez reconstruire votre application 32 bits en tant qu’application 64 bits. Pour plus d’informations sur la prise en charge de MAPI pour Outlook 64 bits, consultez [Génération d’applications MAPI sur des plateformes 32 bits et 64 bits](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).

- **Exemple de fournisseur de magasin** de messages : l’exemple de [fournisseur de magasin PST encapsulé](message-store-provider-sample.md) avait été précédemment mis à jour pour prendre en charge l’architecture 64 bits. La rubrique Sur [l’initialisation d’un fournisseur de magasin PST encapsulé](initializing-a-wrapped-pst-store-provider.md) a été développée pour fournir des informations sur les chemins PST et Unicode encapsulés.

- **Flux de saisie semi-automatique** : la rubrique du [cache de surnoms](nickname-cache.md) , anciennement le **format de fichier Nk2**, a été mise à jour pour refléter les modifications apportées à Outlook 2013 et Outlook 2010. Des informations telles que la liste de saisie semi-automatique, qui est la liste des noms qui s’affiche dans les zones d’édition **To**, **Cc** et **Cci** pendant qu’un utilisateur compose un e-mail, sont désormais enregistrées dans le [flux de saisie semi-automatique](autocomplete-stream.md) d’un message sur l’ordinateur local au lieu de l’enregistrer dans un fichier comme dans Outlook 2007.

  - Interaction avec le flux de saisie semi-automatique

  - Chargement du flux de saisie semi-automatique

  - Enregistrement du flux de saisie semi-automatique

- **Prise en charge de l’arrêt rapide pour les clients MAPI** : les clients MAPI peuvent désormais lancer un arrêt rapide et faire en sorte que le sous-système MAPI avertisse les fournisseurs chargés pour réduire la perte de données suite à l’arrêt rapide. Des interfaces supplémentaires ont été ajoutées pour le client et le fournisseur afin de prendre en charge l’arrêt rapide. Pour plus d’informations sur l’arrêt rapide, consultez [Arrêt du client dans MAPI](client-shutdown-in-mapi.md).

- **Structure de flux pour les définitions de champ pour un élément Outlook** : la documentation d’un flux binaire pour la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) a été ajoutée. Cette propriété spécifie les définitions de tous les champs personnalisés et des paramètres de liaison de données pour les champs intégrés d’un élément Outlook.

- **Remplacement du magasin personnel** : les interfaces suivantes et leurs méthodes respectives ont été ajoutées pour prendre en charge la substitution de la stratégie PST (Personal Folders File) des fournisseurs de **magasins PSTDisableGrow** :

    [IPSTOVERRIDEQ::IUnknown](ipstoverridereqiunknown.md)

    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)

- **Utilisation de plusieurs comptes Exchange** : la documentation de [l’API carnet d’adresses MAPI](using-multiple-exchange-accounts.md) a été ajoutée. Cette API a été améliorée pour prendre en charge plusieurs comptes Exchange dans Microsoft Outlook 2010 et inclut désormais Microsoft Outlook 2013. R�soudre les adresses correctement avec plusieurs comptes Exchange, utilisez les nouvelles fonctions qui utilisent un contexte de compte afin que les appels vers le carnet d'adresses rechercher le compte Exchange appropri�.

- **Formats de fichier MAPI** : les informations de configuration MAPI ont été développées pour expliquer comment vous pouvez utiliser des chemins d’accès dans [l’inscription des services et des fournisseurs de services dans MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md).

- **Propriétés** : les propriétés étiquetées suivantes ont été ajoutées en plus de la documentation relative à 38 autres propriétés marquées et propriétés nommées qui avaient été ajoutées précédemment :

  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)

  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)

  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)

  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)

  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)

  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)

- **Constantes MAPI** : les [constantes MAPI](mapi-constants.md) consolidées ont été développées. Dans les versions précédentes, elles étaient distribuées dans un certain nombre de rubriques, mais elles sont maintenant collectées dans une seule rubrique pour faciliter leur découverte et leur utilisation. Ils ont également été étendus pour offrir une couverture plus étendue, notamment les sections suivantes :

  - Définitions du carnet d’adresses Exchange et des codes d’erreur du magasin de messages

  - Définitions des quotas de mode mis en cache de boîte aux lettres Exchange Server

## <a name="see-also"></a>Voir aussi

[Mise en route avec la référence de MAPI pour Outlook 2013](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

---
title: Nouveautés de cette édition
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 23a8b84af50cc8a046206ab37144d84c4c9b6d56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329546"
---
# <a name="whats-new-in-this-edition"></a>Nouveautés de cette édition

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La référence MAPI Microsoft Outlook 2013 a été mise à jour afin d'inclure de la documentation pour diverses nouvelles fonctionnalités. 
  
## <a name="new-content"></a>Nouveau contenu

Du contenu a été ajouté pour les fonctionnalités suivantes:
  
- La rubrique [Getting Started with the outlook 2013 MAPI Reference](getting-started-with-the-outlook-mapi-reference.md) a été mise à jour pour faire référence à des informations complètes sur les modèles de programmation pour vos fonctionnalités Outlook et MAPI afin de vous aider à identifier les API et les technologies les plus utilisées fonction de vos besoins. Les liens vers l'article technique référencé ont également été modifiés dans les rubriques suivantes: 
    
  - [Référence MAPI Outlook](outlook-mapi-reference.md)
    
  - [Vue d'ensemble de r�f�rence de MAPI Outlook 2013](outlook-mapi-reference-overview.md)
    
- **Exemple de fournisseur de banque de messages**: l'exemple de code de [fournisseur de banque de fichiers PST encapsulé](message-store-provider-sample.md) a été révisé pour reconnaître et prendre en compte Outlook 2013. Pour plus d'informations, reportez-vous à contenu précédemment révisé dans cette rubrique. 
    
- **Flux de saisie semi-automatique**: la rubrique du [cache](nickname-cache.md) des surnoms, ancienneMent le **format de fichier Nk2**, a été mise à jour pour refléter les modifications apportées dans outlook 2013, ainsi qu'Outlook 2010. Les rubriques suivantes ont été révisées afin de fournir des informations sur le format de fichier. nk2 conseils pour les développeurs pour Microsoft Outlook 2003/Microsoft Office Outlook 2007 et l'analyse de fichiers binaires. Pour plus d'informations, reportez-vous à contenu précédemment révisé dans cette rubrique.
    
  - [Profils MAPI](mapi-profiles.md)
    
  - [Cache de surnoms](nickname-cache.md)
    
  - [Flux de saisie semi-automatique](autocomplete-stream.md)
    
- **Interfaces**-la rubrique [IAddrBook:: OpenEntry](iaddrbook-openentry.md) documente une méthode d'ouverture d'une entrée de carnet d'adresses et en renvoyant un pointeur vers l'interface utilisée pour y accéder. Il contenait auparavant un indicateur dans le paramètre *ulFlags* , **MAPI_GAL_ONLY**, qui pouvait être utilisé pour ouvrir la liste d'adresses globale (LAG), uniquement, et a été modifié pour inclure sa définition.
    
- **Propriétés**— la rubrique **PR_CONVERSATION_KEY** nommée Property ([propriété canonique PidTagConversationKey](pidtagconversationkey-canonical-property.md)) a été ajoutée et est liée à **IPM. **Les messages de MessageManager dans Outlook MAPI uniquement. Les rubriques suivantes qui s'y rapportent et la documentation sur le flux TNEF (Transport-Neutral Encapsulation Format) ont été modifiées: 
    
  - [Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Mappage des attributs TNEF aux propriétés MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID et attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Contenu révisé précédemment

Le contenu a été ajouté dans les versions précédentes de la référence MAPI Outlook pour les fonctionnalités suivantes:
  
- Microsoft Outlook 2013 permet des scénarios de déploiement non traditionnels, tels que Side-Side et «démarrer en un clic». Ces scénarios peuvent compliquer la logique utilisée pour charger la bibliothèque MAPI appropriée. Les développeurs MAPI ont désormais la possibilité de lier explicitement aux fonctions MAPI et de créer explicitement un lien vers le stub MAPI du client MAPI par défaut (par exemple, msmapi32. dll d'Outlook) sans passer par la bibliothèque MAPI et le stub MAPI Windows. Pour plus d'informations sur la liaison explicite par rapport à la liaison implicite, voir [lien vers des fonctions MAPI](how-to-link-to-mapi-functions.md). La **bibliothèque de stub MAPI**, publiée sur le site Web [CodePlex](https://mapistublibrary.codeplex.com/) , fournit un remplacement de la fonction Mapi32. lib qui prend en charge la génération d'applications MAPI 32 bits et 64 bits. 
    
- **Prise en charge de Microsoft Outlook 64 bits**— des rubriques de référence pour les éléments d'API applicables ont été mises à jour pour correspondre aux nouveaux fichiers d'en-tête qui prennent en charge l'Outlook 64 bits. Ces fichiers d'en-tête sont disponibles en tant que téléchargement dans [Outlook 2010: fichiers d'en-tête MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Un nouvel exemple de code a été fourni dans [Vérifier la version d'Outlook](how-to-check-the-version-of-outlook.md) pour montrer comment vérifier si la version installée d'outlook est 64 bits Microsoft Outlook 2010 et a été modifiée pour Outlook 2013. Si votre application MAPI 32 bits existante est exécutée sur un système d'exploitation 64 bits avec Outlook 64 bits installé, vous devrez recréer votre application 32 bits en tant qu'application 64 bits. Pour plus d'informations sur la prise en charge de MAPI pour Outlook 64 bits, consultez la rubrique [création d'applications MAPI sur les plateformes 32 bits et 64](building-mapi-applications-on-32-bit-and-64-bit-platforms.md)bits.
    
- **Exemple de fournisseur de banque de messages**: l' [exemple de fournisseur de banque de fichiers PST encapsulé](message-store-provider-sample.md) a déjà été mis à jour pour prendre en charge l'architecture 64 bits. La rubrique relative à l' [initialisation d'un fournisseur de magasins de dossiers personnels (PST) encapsulé](initializing-a-wrapped-pst-store-provider.md) a été développée pour fournir des informations sur les chemins d'accès aux fichiers PST et Unicode. 
    
- **Flux de saisie semi-automatique**— la rubrique du [cache](nickname-cache.md) des surnoms, ancienneMent le **format de fichier Nk2**, a été mise à jour pour refléter les modifications apportées dans Outlook 2013, ainsi que dans Outlook 2010. Des informations telles que la liste de saisie semi-automatique, qui est la liste des noms qui s'affichent dans les zones **d'édition à**, **CC**et **CCI** pendant qu'un utilisateur rédige un courrier électronique, est désormais enregistrée dans le [flux de saisie semi-automatique](autocomplete-stream.md) d'un message sur l'ordinateur local. au lieu de l'enregistrer dans un fichier comme dans Outlook 2007. 
    
  - Interaction avec le flux de saisie semi-automatique
    
  - Chargement du flux de saisie semi-automatique
    
  - Enregistrement du flux de saisie semi-automatique
    
- **Prise en charge de l'arrêt rapide pour les clients MAPI**: les clients MAPI peuvent désormais lancer un arrêt rapide et demander au sous-système MAPI de notifier les fournisseurs chargés de réduire les pertes de données de l'arrêt rapide. Des interfaces supplémentaires ont été ajoutées pour le client et le fournisseur afin de prendre en charge la mise à l'arrêt rapide. Pour plus d'informations sur l'arrêt rapide, consultez la rubrique [arrêt du client dans MAPI](client-shutdown-in-mapi.md).
    
- **Structure de flux pour les définitions de champ pour un élément Outlook**— la documentation relative à un flux binaire pour la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) a été ajoutée. Cette propriété spécifie les définitions de tous les champs personnalisés et des paramètres de liaison de données pour les champs prédéfinis d'un élément Outlook. 
    
- **Remplacement du magasin personnel**: les interfaces suivantes et leurs méthodes respectives ont été ajoutées pour prendre en charge le remplacement de la stratégie **PSTDisableGrow** des fournisseurs de magasins de fichiers de dossiers personnels (PST): 
    
    [IPSTOVERRIDEREQ:: IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1:: IUnknown](ipstoverride1iunknown.md)
    
- **Utilisation de plusieurs comptes Exchange**: la documentation de l' [API de carnet d'adresses MAPI](using-multiple-exchange-accounts.md) a été ajoutée. Cette API a été améliorée pour prendre en charge plusieurs comptes Exchange dans Microsoft Outlook 2010 et inclut désormais Microsoft Outlook 2013. R�soudre les adresses correctement avec plusieurs comptes Exchange, utilisez les nouvelles fonctions qui utilisent un contexte de compte afin que les appels vers le carnet d'adresses rechercher le compte Exchange appropri�. 
    
- **Formats de fichiers MAPI**: des informations de configuration MAPI ont été développées pour expliquer comment vous pouvez utiliser les chemins d'accès dans la procédure d' [inscription des services et des fournisseurs de services dans MapiSvc. inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propriétés**: les propriétés marquées suivantes ont été ajoutées en plus de la documentation pour 38 autres propriétés marquées et des propriétés nommées qui ont été précédemment ajoutées:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes MAPI**: les [constantes MAPI](mapi-constants.md) consolidées ont été développées. Dans les versions précédentes, ils étaient distribués dans un certain nombre de sujets, mais sont désormais collectés dans une seule rubrique pour les rendre plus faciles à découvrir et à utiliser. Elles ont également été développées afin de fournir une couverture plus étendue, notamment les sections suivantes: 
    
  - Définitions des codes d'erreur du carnet d'adresses Exchange et de la Banque de messages
    
  - Définitions des quotas du mode de mise en cache des boîtes aux lettres Exchange Server
    
## <a name="see-also"></a>Voir aussi



[Mise en route avec la référence de MAPI pour Outlook 2013](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)


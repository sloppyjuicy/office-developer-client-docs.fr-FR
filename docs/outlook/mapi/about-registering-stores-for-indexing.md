---
title: À propos de l'enregistrement des magasins pour l'indexation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321825"
---
# <a name="about-registering-stores-for-indexing"></a>À propos de l'enregistrement des magasins pour l'indexation

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique est propre à la recherche instantanée dans Microsoft Office Outlook 2007.
  
La recherche instantanée vous permet de trouver rapidement des éléments dans Outlook. Il utilise des composants de Windows Desktop Search.
  
Le gestionnaire de protocole MAPI vérifie si le Registre Windows contient des magasins qu'il doit indexer à des fins de recherche. Les fournisseurs de banque qui souhaitent être indexés doivent être enregistrés dans le Registre Windows.
  
Par défaut, Windows Desktop Search ajoute les quatre types de fournisseurs de banque suivants au registre Windows pour permettre l'indexation:
  
- Stocker les fichiers de dossiers personnels (. PST).
    
-  Banque Microsoft Exchange, y compris les fichiers de dossiers en mode hors connexion (. ost). 
    
-  Stockez les dossiers publics. 
    
-  Stockez Microsoft Office Outlook Connector pour MSN. 
    
 Les fournisseurs de magasin tiers qui souhaitent être indexés doivent s'enregistrer dans le Registre Windows. 
  
> [!NOTE]
> Les administrateurs et les utilisateurs peuvent utiliser un paramètre de stratégie de groupe pour empêcher la recherche sur le bureau Windows d'indexer les éléments Outlook. Pour plus d'informations, consultez la rubrique [extension de Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Clés de Registre

Sur un ordinateur, tous les fournisseurs de magasin qui souhaitent être indexés doivent être enregistrés sous une seule des trois clés de Registre suivantes dans le Registre Windows. Le gestionnaire de protocole MAPI regarde sous chacune de ces clés dans l'ordre suivant:
  
1. [HKLM] \Software\Policies\Microsoft\Windows\Windows Search \
    
2. [HKLM] \Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU] \Software\Microsoft\Windows\Windows Search\Preferences\
    
 Chaque valeur sous la clé correspond à un fournisseur de banque d'index qui sera indexé. Le nom de la valeur est l'identificateur global unique (GUID) du fournisseur de banque, qui est de type **DWORD** et possède la valeur hexadécimale 0x00000001. 
  
## <a name="guids-for-store-providers"></a>GUID pour les fournisseurs de magasin

La propriété MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** spécifie le GUID d'un magasin MAPI. Les GUID des fournisseurs de magasins qu'ils indexent sont décrits dans le tableau suivant. 
  
||||
|:-----|:-----|:-----|
|**Type de fournisseur de banque** <br/> |**GUID** <br/> |**Notes** <br/> |
|Fichiers de dossiers personnels (. DOSSIERS  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID est documenté dans le fichier d'en-tête public MSPST. h en tant que **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID est documenté dans le fichier d'en-tête public edkmdb. h en tant que **pbExchangeProviderPrimaryUserGuid** <br/> |
|Dossiers publics  <br/> |{70fab278-f7af-CD11-9bc8-00aa002fc45a}  <br/> |GUID est documenté dans le fichier d'en-tête public edkmdb. h en tant que **pbExchangeProviderPublicGuid** <br/> |
|Outlook Connector pour MSN  <br/> |{c34f5c97-eb05-bb4b-B199-2a7570ec7cf9}  <br/> |Aucun  <br/> |
   
## <a name="see-also"></a>Voir aussi



[À propos de l’API de magasin](about-the-store-api.md)


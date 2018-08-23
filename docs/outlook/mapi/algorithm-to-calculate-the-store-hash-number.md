---
title: Algorithme permettant de calculer le nombre de hachages de magasin
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 489e0d74-8ecd-23ba-c874-18fd8c50fd12
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 84065c1441008732380e68d9786d7844dbb64cb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592100"
---
# <a name="algorithm-to-calculate-the-store-hash-number"></a><span data-ttu-id="d6d18-103">Algorithme permettant de calculer le nombre de hachages de magasin</span><span class="sxs-lookup"><span data-stu-id="d6d18-103">Algorithm to Calculate the Store Hash Number</span></span>
 
<span data-ttu-id="d6d18-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6d18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6d18-105">Dans le cadre d’un MAPI URL Uniform Resource Locator (), un fournisseur de banque envoie un numéro de hachage magasin au Gestionnaire de protocole MAPI pour identifier un objet est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="d6d18-105">As part of a MAPI Uniform Resource Locator (URL), a store provider sends a store hash number to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="d6d18-106">Le Gestionnaire de protocole MAPI utilise ce numéro de hachage magasin pour identifier un magasin.</span><span class="sxs-lookup"><span data-stu-id="d6d18-106">The MAPI Protocol Handler uses this store hash number to identify a store.</span></span> <span data-ttu-id="d6d18-107">En règle générale, un fournisseur de magasins calcule le nombre de hachage de magasin en fonction de la signature de mappage banque, si le magasin de la propriété **[PR_MAPPING_SIGNATURE](pidtagmappingsignature-canonical-property.md)** définie dans la section profil global.</span><span class="sxs-lookup"><span data-stu-id="d6d18-107">In general, a store provider calculates the store hash number based on the store mapping signature, if the store has the **[PR_MAPPING_SIGNATURE](pidtagmappingsignature-canonical-property.md)** property defined in the global profile section.</span></span> <span data-ttu-id="d6d18-108">Sinon, le fournisseur de banque utilise l’ID d’entrée de magasin.</span><span class="sxs-lookup"><span data-stu-id="d6d18-108">Otherwise, the store provider uses the store entry ID.</span></span> <span data-ttu-id="d6d18-109">L’algorithme pour calculer le nombre de hachage magasin doit réduire ambiguïtés qui identifie les magasins.</span><span class="sxs-lookup"><span data-stu-id="d6d18-109">The algorithm to calculate the store hash number must minimize ambiguities identifying stores.</span></span> 
  
<span data-ttu-id="d6d18-110">Cette rubrique décrit un algorithme que Microsoft Office Outlook pour calculer un numéro de hachage magasin en fonction de l’ID de signature ou l’entrée de mappage store et le nom de fichier du magasin.</span><span class="sxs-lookup"><span data-stu-id="d6d18-110">This topic describes an algorithm that Microsoft Office Outlook uses to calculate a store hash number based on the store mapping signature or entry ID and the store file name.</span></span> 
  
<span data-ttu-id="d6d18-111">Le blob doivent être codées est la propriété PR_ENTRYID de la banque dans la plupart des cas, mais pour les banques Exchange mis en cache, à la fois publics et privés, le blob doivent être le PR_MAPPING_SIGNATURE, trouvé dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d6d18-111">The binary blob to be encoded is the PR_ENTRYID of the store in most cases, but for cached Exchange stores, both public and private, the binary blob should be the PR_MAPPING_SIGNATURE, found in the profile.</span></span>
  
<span data-ttu-id="d6d18-112">Après le calcul de hachage pour blob binaire de banque de dossiers publics, mais avant le hachage le chemin d’accès de fichier OST, la constante 0x2E505542, qui représente la chaîne «. La composition », est hachage dans pour s’assurer qu’il est unique, qui est différent du hachage de la banque privée.</span><span class="sxs-lookup"><span data-stu-id="d6d18-112">After computing the hash for a public folder store's binary blob, but before hashing-in the OST path, the constant 0x2E505542, which represents the string ".PUB", is hashed in to assure it is unique, that is, distinct from the private store's hash.</span></span>
  
<span data-ttu-id="d6d18-113">Le code de prise en charge puise des pertinents pour des informations à partir du profil, qui peut être utilisé pour déterminer si une banque est publique ou privée, si elle est mise en cache, et le chemin d’accès du fichier OST.</span><span class="sxs-lookup"><span data-stu-id="d6d18-113">The support code culls the relevant bits from the profile, which can be used to determine whether a store is public or private, if it's cached, and the path to the OST.</span></span> <span data-ttu-id="d6d18-114">Pour incorporer ce code dans un projet, appelez la fonction ComputeStoreHash, qui prend comme entrée le pointeur de la session ainsi que PR\_ENTRYID, PR\_SERVICE_UID et PR\_MDB_PROVIDER à partir du message stocker la table.</span><span class="sxs-lookup"><span data-stu-id="d6d18-114">To incorporate this code in a project, call the function ComputeStoreHash, which takes as its input the session pointer as well as PR\_ENTRYID, PR\_SERVICE_UID, and PR\_MDB_PROVIDER from the message store table.</span></span> <span data-ttu-id="d6d18-115">Le reste des informations nécessaires qu’il obtient à partir du profil.</span><span class="sxs-lookup"><span data-stu-id="d6d18-115">The rest of the information it needs it gets from the profile.</span></span> <span data-ttu-id="d6d18-116">Pour la sortie, cette fonction renvoie la valeur de hachage calculé à partir de PR\_MAPPING_SIGNATURE si la banque est une banque d’informations Exchange mis en cache, ou le hachage calculé à partir de PR\_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="d6d18-116">For output, this function returns the hash as computed from PR\_MAPPING_SIGNATURE if the store is a cached Exchange store, or the hash as computed from PR\_ENTRYID.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d6d18-117">La fonction de prise en charge HrEmsmdbUIDFromStore est un [Plusieurs comptes Exchange](using-multiple-exchange-accounts.md)-remplacement connaissance de pbGlobalProfileSectionGuid pour ouvrir la section de profil pour une boîte aux lettres Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6d18-117">The HrEmsmdbUIDFromStore support function is a [Multiple Exchange Accounts](using-multiple-exchange-accounts.md)-aware replacement for using pbGlobalProfileSectionGuid to open the profile section for an Exchange mailbox.</span></span> 
  
```cpp
#define PR_PROFILE_OFFLINE_STORE_PATH_A PROP_TAG(PT_STRING8, 0x6610)
#define PR_PROFILE_OFFLINE_STORE_PATH_W PROP_TAG(PT_UNICODE, 0x6610)
#define CONFIG_OST_CACHE_PRIVATE  ((ULONG)0x00000180)
#define CONFIG_OST_CACHE_PUBLIC   ((ULONG)0x00000400)
HRESULT HrEmsmdbUIDFromStore(IMAPISession* pmsess,
                             MAPIUID* puidService,
                             MAPIUID* pEmsmdbUID)
{
  if (!puidService) return MAPI_E_INVALID_PARAMETER;
  HRESULT hRes = S_OK;
  SRestriction mres = {0};
  SPropValue mval = {0};
  SRowSet* pRows = NULL;
  SRow* pRow = NULL;
  LPSERVICEADMIN spSvcAdmin = NULL;
  LPMAPITABLE spmtab = NULL;
  enum { eEntryID = 0, eSectionUid, eMax };
  static const SizedSPropTagArray(eMax, tagaCols) =
  {
    eMax,
    {
      PR_ENTRYID,
      PR_EMSMDB_SECTION_UID,
    }
  };
  hRes = pmsess->AdminServices(0, (LPSERVICEADMIN*)&spSvcAdmin);
  if (SUCCEEDED(hRes) && spSvcAdmin)
  {
    hRes = spSvcAdmin->GetMsgServiceTable(0, &spmtab);
    if (spmtab)
    {
      hRes = spmtab->SetColumns((LPSPropTagArray)&tagaCols, TBL_BATCH);
      mres.rt = RES_PROPERTY;
      mres.res.resProperty.relop = RELOP_EQ;
      mres.res.resProperty.ulPropTag = PR_SERVICE_UID;
      mres.res.resProperty.lpProp = &mval;
      mval.ulPropTag = PR_SERVICE_UID;
      mval.Value.bin.cb = sizeof(*puidService);
      mval.Value.bin.lpb = (LPBYTE)puidService;
      (void) spmtab->Restrict(&mres, 0);
      (void) spmtab->QueryRows(10, 0, &pRows);
      if (SUCCEEDED(hRes) && pRows && pRows->cRows)
      {
        pRow = &pRows->aRow[0];
        if (pEmsmdbUID && pRow)
        {
          if (PR_EMSMDB_SECTION_UID == pRow->lpProps[eSectionUid].ulPropTag &&
            pRow->lpProps[eSectionUid].Value.bin.cb == sizeof(*pEmsmdbUID))
          {
            memcpy(pEmsmdbUID, pRow->lpProps[eSectionUid].Value.bin.lpb, sizeof(*pEmsmdbUID));
          }
        }
      }
      FreeProws(pRows);
    }
    if (spmtab) spmtab->Release();
  }
  if (spSvcAdmin) spSvcAdmin->Release();
  return hRes;
} // HrEmsmdbUIDFromStore
bool FExchangePrivateStore(LPMAPIUID lpmapiuid)
{
  if (!lpmapiuid) return false;
  return IsEqualMAPIUID(lpmapiuid, (LPMAPIUID)pbExchangeProviderPrimaryUserGuid);
} // FExchangePrivateStore
bool FExchangePublicStore(LPMAPIUID lpmapiuid)
{
  if (!lpmapiuid) return false;
  return IsEqualMAPIUID(lpmapiuid, (LPMAPIUID)pbExchangeProviderPublicGuid);
} // FExchangePublicStore
DWORD ComputeHash(ULONG cbStoreEID, LPBYTE pbStoreEID, LPCSTR pszFileName, LPCWSTR pwzFileName, BOOL bPublicStore)
{
  DWORD  dwHash = 0;
  ULONG  cdw    = 0;
  DWORD* pdw    = NULL;
  ULONG  cb     = 0;
  BYTE*  pb     = NULL;
  ULONG  i      = 0;
  if (!cbStoreEID || !pbStoreEID) return dwHash;
  // Shouldn't see both of these at the same time.
  if (pszFileName && pwzFileName) return dwHash;
  // Get the Store Entry ID
  // pbStoreEID is a pointer to the Entry ID.
  // cbStoreEID is the size in bytes of the Entry ID.
  pdw = (DWORD*)pbStoreEID;
  cdw = cbStoreEID / sizeof(DWORD);
  for (i = 0; i < cdw; i++)
  {
    dwHash = (dwHash << 5) + dwHash + *pdw++;
  }
  pb = (BYTE *)pdw;
  cb = cbStoreEID % sizeof(DWORD);
  for (i = 0; i < cb; i++)
  {
    dwHash = (dwHash << 5) + dwHash + *pb++;
  }
  if (bPublicStore)
  {
    // Augment to assure it is unique, else could be same as private store.
    dwHash = (dwHash << 5) + dwHash + 0x2E505542; // this is '.PUB'
  }
  // To also include the store file name in the hash calculation,
  // pszFileName and pwzFileName are NULL terminated strings with the path and filename of the store.
  if (pwzFileName)
  {
    while (*pwzFileName)
    {
      dwHash = (dwHash << 5) + dwHash + *pwzFileName++;
    }
  }
  else if (pszFileName)
  {
    while (*pszFileName)
    {
      dwHash = (dwHash << 5) + dwHash + *pszFileName++;
    }
  }
  // dwHash now contains the hash to be used. It should be written in hex when building a URL.
  return dwHash;
} // ComputeHash
void ComputeStoreHash(LPMAPISESSION lpMAPISession, LPSBinary lpEntryID, LPSBinary lpServiceUID, LPSBinary lpProviderUID, DWORD* lpdwSigHash, DWORD* lpdwEIDHash)
{
  HRESULT hRes = S_OK;
  MAPIUID emsmdbUID = {0};
  LPPROFSECT lpProfSect = NULL;
  BOOL fPublicExchangeStore  = FExchangePublicStore((LPMAPIUID)lpProviderUID->lpb);
  BOOL fPrivateExchangeStore = FExchangePrivateStore((LPMAPIUID)lpProviderUID->lpb);
  BOOL fCached = false;
  LPSPropValue lpConfigProp = NULL;
  LPSPropValue lpPathPropA = NULL;
  LPSPropValue lpPathPropW = NULL;
  LPSPropValue lpMappingSig = NULL;
  LPSTR szPath = NULL; // Do not free.
  LPWSTR wzPath = NULL; // Do not free.
  // Get profile section.
  if (lpServiceUID)
  {
    hRes = HrEmsmdbUIDFromStore(lpMAPISession,
      (LPMAPIUID) lpServiceUID->lpb,
      &emsmdbUID);
    if (SUCCEEDED(hRes))
    {
      hRes = lpMAPISession->OpenProfileSection(&emsmdbUID, NULL, 0, &lpProfSect);
    }
  }
  if (!lpServiceUID || FAILED(hRes))
  {
    // For Outlook 2003/2007, HrEmsmdbUIDFromStore may not succeed,
    // so use pbGlobalProfileSectionGuid instead.
    hRes = lpMAPISession->OpenProfileSection((LPMAPIUID)pbGlobalProfileSectionGuid, NULL, 0, &lpProfSect);
  }
  if (lpProfSect)
  {
    hRes = HrGetOneProp(lpProfSect, PR_PROFILE_CONFIG_FLAGS, &lpConfigProp);
    if (SUCCEEDED(hRes) && PROP_TYPE(lpConfigProp->ulPropTag) != PT_ERROR)
    {
      if (fPrivateExchangeStore)
      {
        fCached = ((lpConfigProp->Value.l & CONFIG_OST_CACHE_PRIVATE) != 0);
      }
      if (fPublicExchangeStore)
      {
        fCached = ((lpConfigProp->Value.l & CONFIG_OST_CACHE_PUBLIC) == CONFIG_OST_CACHE_PUBLIC);
      }
    }
    if (fCached)
    {
      hRes = HrGetOneProp(lpProfSect, PR_PROFILE_OFFLINE_STORE_PATH_W, &lpPathPropW);
      if (FAILED(hRes))
      {
        hRes = HrGetOneProp(lpProfSect, PR_PROFILE_OFFLINE_STORE_PATH_A, &lpPathPropA);
      }
      if (SUCCEEDED(hRes))
      {
        if (lpPathPropW && lpPathPropW->Value.lpszW)
        {
          wzPath = lpPathPropW->Value.lpszW;
        }
        else if (lpPathPropA && lpPathPropA->Value.lpszA)
        {
          szPath = lpPathPropA->Value.lpszA;
        }
      }
      // If this is an Exchange store with an OST path, it's an OST, so get the mapping signature.
      if ((fPrivateExchangeStore || fPublicExchangeStore) && (wzPath || szPath))
      {
        hRes = HrGetOneProp(lpProfSect, PR_MAPPING_SIGNATURE, &lpMappingSig);
      }
    }
  }
  DWORD dwSigHash = NULL;
  if (lpMappingSig && PT_BINARY == PROP_TYPE(lpMappingSig->ulPropTag))
  {
    dwSigHash = ComputeHash(lpMappingSig->Value.bin.cb, lpMappingSig->Value.bin.lpb, NULL, NULL, fPublicExchangeStore);
  }
  DWORD dwEIDHash = ComputeHash(lpEntryID->cb, lpEntryID->lpb, szPath, wzPath, fPublicExchangeStore);
  if (lpdwSigHash) *lpdwSigHash = dwSigHash;
  if (lpdwEIDHash) *lpdwEIDHash = dwEIDHash;
  MAPIFreeBuffer(lpMappingSig);
  MAPIFreeBuffer(lpPathPropA);
  MAPIFreeBuffer(lpPathPropW);
  MAPIFreeBuffer(lpConfigProp);
  if (lpProfSect) lpProfSect->Release();
} // ComputeStoreHash
```

> [!TIP]
> <span data-ttu-id="d6d18-118">La fonction HrEmsmdbUIDFromStore fonctionne sans réellement ouvrir le magasin, afin qu’il soit une approche de bon usage général.</span><span class="sxs-lookup"><span data-stu-id="d6d18-118">The HrEmsmdbUIDFromStore function works without actually opening the store, so it is a good general purpose approach.</span></span> <span data-ttu-id="d6d18-119">Toutefois, si vous avez déjà un pointeur vers l’objet store, vous pouvez également récupérer la section profil GUID directement à partir de la banque de messages par la lecture de la propriété PR_EMSMDB_SECTION_UID.</span><span class="sxs-lookup"><span data-stu-id="d6d18-119">However, if you have a pointer to the store object already, you can also retrieve the profile section GUID directly from the message store by reading the PR_EMSMDB_SECTION_UID property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6d18-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6d18-120">See also</span></span>

- [<span data-ttu-id="d6d18-121">À propos de l’indexation de magasin basée sur une notification</span><span class="sxs-lookup"><span data-stu-id="d6d18-121">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
- [<span data-ttu-id="d6d18-122">À propos des URL MAPI pour l’indexation basée sur une notification</span><span class="sxs-lookup"><span data-stu-id="d6d18-122">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)


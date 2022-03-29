```java
public class BaseRepositoryServiceImplTest  
{  
  @Mock  
 private Session session;  
  
 @Mock  
 private QueryManager queryManager;  
  
 @Mock  
 private NonConformanceService ncrService;  
  
 @Mock  
 private NonConformanceDAO ncrDao;  
  
 @InjectMocks  
 private BaseRepositoryServiceImpl baseRepositoryService;  
  
 @BeforeEach  
 public void setup()  
  {  
    MockitoAnnotations.initMocks(this);  
 }  
  
  @Test  
 public void uploadQualityItem_ncrRelatedFileUploaded_ListWithPfcsReturnedJustOne() throws IOException, RepositoryException  
 {  
    // prepare  
	// The spy does the work!!!
 BaseRepositoryServiceImpl baseRepositoryServiceTest = Mockito.spy(baseRepositoryService);  
  
 String fileName = "myFile.txt";  
 QualityType qualityType = QualityType.NON_CONFORMANCE;  
 long id = 12L;  
 MultipartFile file = new MockMultipartFile(fileName, new byte[] {12, 23});  
  
 NonConformance ncr = new NonConformance();  
 when(ncrService.findById(id)).thenReturn(ncr);  
 when(ncrDao.save(ncr)).thenReturn(ncr);  
  
 Node node = mock(Node.class);  
  
 doReturn(node).when(baseRepositoryServiceTest).uploadFileToPath(any(), any());  
 // act  
 baseRepositoryServiceTest.uploadQualityItem(fileName, qualityType, id, file.getInputStream());  
  
 // assert  
  
 }  
}
```
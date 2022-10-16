import java.time.LocalDate;
import java.time.LocalDateTime;
import java.time.format.DateTimeFormatter;
import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

public class Main {
    public static void main(String[] args){
        ArrayList<Employee>employees=new ArrayList<>();
        // Nhân viên một
        Employee nv=new Employee();
        LocalDate date1 = LocalDate.of(1977, 1,28);
        nv.setId("Nv01");
        nv.setTen("Trần Văn Đêm");
        nv.setNgaysinh(date1);
        nv.setGioitinh("nam");
        nv.setLuong(10.000);
        // Nhân viên hai
        Employee nv1=new Employee();
        LocalDate date = LocalDate.of(1987, 06,28);
        nv1.setId("Nv02");
        nv1.setTen("Ngô Bích Thảo");
        nv1.setNgaysinh(date);
        nv1.setGioitinh("nữ");
        nv1.setLuong(13.000);
        // Nhân viên ba
        Employee nv2=new Employee();
        LocalDate date2 = LocalDate.of(2000, 1,8);
        nv2.setId("Nv03");
        nv2.setTen("Lê Thị Lệ Diễm");
        nv2.setNgaysinh(date2);
        nv2.setGioitinh("nữ");
        nv2.setLuong(11.500);
        // Nhân viên bốn
        Employee nv3=new Employee();
        LocalDate date3 = LocalDate.of(1981, 12,28);
        nv3.setId("Nv04");
        nv3.setTen("Đinh Trọng Quốc");
        nv3.setNgaysinh(date3);
        nv3.setGioitinh("nam");
        nv3.setLuong(19.000);
        // Nhân viên năm
        Employee nv4=new Employee();
        LocalDate date4 = LocalDate.of(1999, 8,14);
        nv4.setId("Nv05");
        nv4.setTen("Đỗ Văn Thạo");
        nv4.setNgaysinh(date4);
        nv4.setGioitinh("nữ");
        nv4.setLuong(16.000);
        // Lưu giá trị
        employees.add(nv);
        employees.add(nv1);
        employees.add(nv2);
        employees.add(nv3);
        employees.add(nv4);
        System.out.println(employees);
        // tìm nhân viên theo id && tên
        System.out.println("Mời bạn chọn");
        System.out.println("Bạn muốn chọn nhân viên theo tiêu chí:" +
                "\n 1.Theo ID.\n 2.Theo Tên.\n Moi ban chon:");
        int a =new Scanner(System.in).nextInt();
        switch (a){
            case 1:
                System.out.println("Mời bạn nhập ID");
                String nameid=new Scanner(System.in).nextLine();
                for (int i = 0; i< employees.size(); i++){
                    if (employees.get(i).getId().equals(nameid));
                    System.out.println(employees.get(i).toString());
                }
            case 2:
                System.out.println("Mời bạn nhập tên muốn tìm");
                String name=new Scanner(System.in).nextLine();
                for (int j=0;j< employees.size();j++){
                    if (employees.get(j).getTen().contains(name)){
                        System.out.println(employees.get(j).toString());
                    }
                }
        }
        // Đếm số nhân viên nam
        System.out.println("Đếm số nhân viên nam,nữ");
        System.out.println("Bạn muốn tìm xem có bao nhiêu nhân viên:"    +
                "\n 1.Nam .\n 2.Nữ.\n   Moi ban chon:");
        int sex=new Scanner(System.in).nextInt();
        int dem=0;
        int dem1=0;
        switch (sex){
            case 1 :{
            for (int i = 0; i < employees.size(); i++) {
                if (employees.get(i).getGioitinh().equals("nam")) {
                    dem++;
                }
            }
                System.out.println(dem);
            break ;
        }
            case 2 : {
                    for (int j = 0; j < employees.size(); j++) {
                        if (employees.get(j).getGioitinh().equals("nữ")) {
                            dem1++;
                        }
                    }
                        System.out.println(dem1);
                    break;
                }
            }
        System.out.println(dem);
        // Liệt kê nhân viên trên 30 tuổi
        System.out.println("Những nhân viên trên 30 tuổi");
        for (int i = 0; i < employees.size(); i++) {
            if(LocalDate.now().getYear() - employees.get(i).getNgaysinh().getYear() > 30){
                System.out.println(employees.get(i).toString());
            }
        }
    // Nhập tháng bất kì và xem tháng đó có nhân viên nào sinh nhật
        System.out.println("Mời bạn nhập tháng sinh nhật muốn tìm");
        int random =new Scanner(System.in).nextInt();
        for (int j=0;j<employees.size();j++){
            // employees.get(j).getNgaysinh().getMonth() thằng này là kiểu Month, mình muốn so sánh phải quy ra kiểu String để so sánh dùng equal
            //random: thằng này là int kiểu số, muốn đem so sánh vs String thì + "" nó sẽ thành String
            if (employees.get(j).getNgaysinh().getMonth().getValue() == random){
                System.out.println(employees.get(j).toString());
            }
        }
        // In ra top 3 người có lương tháng cao nhất
        System.out.println("In ra top 3 người có lương tháng cao nhất");
        for (int i=0;i<employees.size();i++){
            if (employees.get(i).getLuong() >= 13){
                System.out.println(employees.get(i).toString());
            }
        }
    }
}

